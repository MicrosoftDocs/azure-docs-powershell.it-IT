---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 8516cbecac3cb4c741bb7aea1e93c10f25222b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520330"
---
# <span data-ttu-id="2b20c-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="2b20c-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="2b20c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b20c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b20c-103">Ottiene suggerimenti per il livello dei prezzi per l'aggiornamento di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b20c-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b20c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b20c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b20c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b20c-105">DESCRIPTION</span></span>
<span data-ttu-id="2b20c-106">Il cmdlet **Get-AzureRmSqlServerUpgradeHint** ottiene suggerimenti per il livello dei prezzi per l'aggiornamento di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b20c-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="2b20c-107">I suggerimenti possono contenere il pool di database elastici e i suggerimenti per i database autonomi.</span><span class="sxs-lookup"><span data-stu-id="2b20c-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="2b20c-108">I database ancora in livelli Web e business pricing ottengono un suggerimento per l'aggiornamento ai nuovi livelli di prezzo di base, standard o Premium o per accedere al pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="2b20c-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="2b20c-109">Questo cmdlet restituisce i suggerimenti per tutti i database ospitati nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="2b20c-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="2b20c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b20c-110">EXAMPLES</span></span>

### <span data-ttu-id="2b20c-111">Esempio 1: ottenere suggerimenti combinati</span><span class="sxs-lookup"><span data-stu-id="2b20c-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="2b20c-112">Questo comando consente di ottenere suggerimenti combinati per tutti i database in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="2b20c-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="2b20c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b20c-113">PARAMETERS</span></span>

### <span data-ttu-id="2b20c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b20c-114">-DefaultProfile</span></span>
<span data-ttu-id="2b20c-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2b20c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b20c-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="2b20c-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="2b20c-117">Indica se i database inclusi nei pool di database elastici devono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="2b20c-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b20c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b20c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b20c-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="2b20c-119">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b20c-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2b20c-120">-ServerName</span></span>
<span data-ttu-id="2b20c-121">Specifica il nome del server per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2b20c-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b20c-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b20c-122">-Confirm</span></span>
<span data-ttu-id="2b20c-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b20c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b20c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b20c-124">-WhatIf</span></span>
<span data-ttu-id="2b20c-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b20c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b20c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b20c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b20c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b20c-127">CommonParameters</span></span>
<span data-ttu-id="2b20c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b20c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b20c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b20c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b20c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b20c-130">INPUTS</span></span>

### <span data-ttu-id="2b20c-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b20c-131">None</span></span>
<span data-ttu-id="2b20c-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2b20c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b20c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b20c-133">OUTPUTS</span></span>

## <span data-ttu-id="2b20c-134">Note</span><span class="sxs-lookup"><span data-stu-id="2b20c-134">NOTES</span></span>

## <span data-ttu-id="2b20c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b20c-135">RELATED LINKS</span></span>

[<span data-ttu-id="2b20c-136">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="2b20c-136">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="2b20c-137">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="2b20c-137">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="2b20c-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2b20c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


