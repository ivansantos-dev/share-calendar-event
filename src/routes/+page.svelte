<script lang="ts">
	    import { page } from '$app/stores';

import '@picocss/pico'
import 'add-to-calendar-button'

const title = $page.url.searchParams.get('title')
const location = $page.url.searchParams.get('location')
const startDate = $page.url.searchParams.get('startdate')
const endDate = $page.url.searchParams.get('enddate')
const startTime = $page.url.searchParams.get('starttime')
const endTime = $page.url.searchParams.get('endtime')
const timeZone = $page.url.searchParams.get('timezone')
</script>

<main class="container">
	<article>
		<h1>Share Calendar Event</h1>
		<div class="grid">
			<table>
				<tr>
					<th>Title</th>
					<td>{title}</td>
				</tr>
				<tr>
					<th>Location</th>
					<td>{location}</td>
				</tr>
				<tr>
					<th>Start date</th>
					<td>{startDate}</td>
				</tr>
				<tr>
					<th>End date</th>
					<td>{endDate}</td>
				</tr>
				<tr>
					<th>Start time</th>
					<td>{startTime}</td>
				</tr>
				<tr>
					<th>End time</th>
					<td>{endTime}</td>
				</tr>
				<tr>
					<th>Timezone</th>
					<td>{timeZone}</td>
				</tr>
			<tr>
			</table>
			<add-to-calendar-button
				name={title}
				options="'Apple','Google','iCal','Outlook.com','Yahoo'"
				location={location}
				startDate={startDate}
				endDate={endDate}
				startTime={startTime}
				endTime={endTime}
				timeZone={timeZone}
				buttonsList
			></add-to-calendar-button>
		</div>
	</article>
</main>
