---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018736"
---
# <span data-ttu-id="4d9c0-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="4d9c0-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="4d9c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d9c0-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9c0-103">Ottiene suggerimenti per il livello dei prezzi per l'aggiornamento di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="4d9c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d9c0-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d9c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d9c0-105">DESCRIPTION</span></span>
<span data-ttu-id="4d9c0-106">Il cmdlet **Get-AzSqlServerUpgradeHint** ottiene suggerimenti per il livello dei prezzi per l'aggiornamento di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="4d9c0-107">I suggerimenti possono contenere il pool di database elastici e i suggerimenti per i database autonomi.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="4d9c0-108">I database ancora in livelli Web e business pricing ottengono un suggerimento per l'aggiornamento ai nuovi livelli di prezzo di base, standard o Premium o per accedere al pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="4d9c0-109">Questo cmdlet restituisce i suggerimenti per tutti i database ospitati nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="4d9c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d9c0-110">EXAMPLES</span></span>

### <span data-ttu-id="4d9c0-111">Esempio 1: ottenere suggerimenti combinati</span><span class="sxs-lookup"><span data-stu-id="4d9c0-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="4d9c0-112">Questo comando consente di ottenere suggerimenti combinati per tutti i database in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="4d9c0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d9c0-113">PARAMETERS</span></span>

### <span data-ttu-id="4d9c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9c0-114">-DefaultProfile</span></span>
<span data-ttu-id="4d9c0-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4d9c0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9c0-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="4d9c0-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="4d9c0-117">Indica se i database inclusi nei pool di database elastici devono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9c0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d9c0-118">-ResourceGroupName</span></span>
<span data-ttu-id="4d9c0-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-119">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9c0-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4d9c0-120">-ServerName</span></span>
<span data-ttu-id="4d9c0-121">Specifica il nome del server per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9c0-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d9c0-122">-Confirm</span></span>
<span data-ttu-id="4d9c0-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9c0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d9c0-124">-WhatIf</span></span>
<span data-ttu-id="4d9c0-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d9c0-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d9c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9c0-127">CommonParameters</span></span>
<span data-ttu-id="4d9c0-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9c0-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d9c0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9c0-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d9c0-130">INPUTS</span></span>

### <span data-ttu-id="4d9c0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d9c0-131">System.String</span></span>

### <span data-ttu-id="4d9c0-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d9c0-132">System.Boolean</span></span>

## <span data-ttu-id="4d9c0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d9c0-133">OUTPUTS</span></span>

### <span data-ttu-id="4d9c0-134">Microsoft. Azure. Commands. SQL. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="4d9c0-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="4d9c0-135">Note</span><span class="sxs-lookup"><span data-stu-id="4d9c0-135">NOTES</span></span>

## <span data-ttu-id="4d9c0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d9c0-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d9c0-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="4d9c0-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="4d9c0-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="4d9c0-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="4d9c0-139">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4d9c0-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


