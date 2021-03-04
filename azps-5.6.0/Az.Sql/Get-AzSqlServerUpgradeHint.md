---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: fc75aa4f838d19044514d3e6c343e04cdbf1d9be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955294"
---
# <span data-ttu-id="0f07f-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="0f07f-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="0f07f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f07f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f07f-103">Ottiene suggerimenti per i prezzi per l'aggiornamento di un server di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0f07f-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="0f07f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f07f-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f07f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f07f-105">DESCRIPTION</span></span>
<span data-ttu-id="0f07f-106">Il cmdlet **Get-AzSqlServerUpgradeHint** ottiene suggerimenti per i prezzi per l'aggiornamento di un server di database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0f07f-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="0f07f-107">I suggerimenti possono contenere il pool di database flessibile e suggerimenti per il database autonomo.</span><span class="sxs-lookup"><span data-stu-id="0f07f-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="0f07f-108">I database ancora in livelli di prezzi Web e Business hanno un suggerimento per passare ai nuovi livelli di prezzi Basic, Standard o Premium o passare al pool di database flessibile.</span><span class="sxs-lookup"><span data-stu-id="0f07f-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="0f07f-109">Questo cmdlet restituisce suggerimenti per tutti i database ospitati nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="0f07f-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="0f07f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f07f-110">EXAMPLES</span></span>

### <span data-ttu-id="0f07f-111">Esempio 1: Ottenere suggerimenti combinati</span><span class="sxs-lookup"><span data-stu-id="0f07f-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="0f07f-112">Questo comando ottiene una combinazione di suggerimenti per tutti i database in un server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="0f07f-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="0f07f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f07f-113">PARAMETERS</span></span>

### <span data-ttu-id="0f07f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f07f-114">-DefaultProfile</span></span>
<span data-ttu-id="0f07f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0f07f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f07f-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="0f07f-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="0f07f-117">Indica se restituire i database inclusi in pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="0f07f-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="0f07f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f07f-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f07f-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="0f07f-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0f07f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f07f-120">-ServerName</span></span>
<span data-ttu-id="0f07f-121">Specifica il nome del server per cui questo cmdlet ottiene un suggerimento per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0f07f-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="0f07f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f07f-122">-Confirm</span></span>
<span data-ttu-id="0f07f-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f07f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f07f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f07f-124">-WhatIf</span></span>
<span data-ttu-id="0f07f-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f07f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f07f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f07f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f07f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f07f-127">CommonParameters</span></span>
<span data-ttu-id="0f07f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f07f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f07f-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f07f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f07f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f07f-130">INPUTS</span></span>

### <span data-ttu-id="0f07f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0f07f-131">System.String</span></span>

### <span data-ttu-id="0f07f-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f07f-132">System.Boolean</span></span>

## <span data-ttu-id="0f07f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f07f-133">OUTPUTS</span></span>

### <span data-ttu-id="0f07f-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="0f07f-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="0f07f-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f07f-135">NOTES</span></span>

## <span data-ttu-id="0f07f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f07f-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f07f-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="0f07f-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="0f07f-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="0f07f-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="0f07f-139">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="0f07f-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


