@Patch('/1') async fixRating(@Body() data: DataDto[]): Promise<void> { await this.restaurantService.fixRating(data); }

@Controller('/api/dining-plan/xyz')

const parserLimit = '50mb'; app.useBodyParser('json', { limit: parserLimit }); app.useBodyParser('urlencoded', { limit: parserLimit, extended: true });

// restaurant rating fix async fixRating(dataDto): Promise<void> { const bulkUpdateOps = dataDto.map(({ id, rating, count }) => ({ updateOne: { filter: { \_id: id }, update: { rating, count }, }, }));

    await this.restaurantModel.bulkWrite(bulkUpdateOps);

}
