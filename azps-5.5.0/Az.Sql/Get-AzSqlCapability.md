---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197774"
---
# <span data-ttu-id="e4948-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e4948-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="e4948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4948-102">SYNOPSIS</span></span>
<span data-ttu-id="e4948-103">Recupera SQL funzionalità di database per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e4948-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="e4948-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4948-104">SYNTAX</span></span>

### <span data-ttu-id="e4948-105">FilterResults (Default)</span><span class="sxs-lookup"><span data-stu-id="e4948-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4948-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="e4948-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4948-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4948-107">DESCRIPTION</span></span>
<span data-ttu-id="e4948-108">Il cmdlet **Get-AzSqlCapability** ottiene le funzionalità di Azure SQL Database sono disponibili nella sottoscrizione corrente per un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="e4948-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="e4948-109">Se si specificano i *parametri ServerVersionName,* *EditionName* o *ServiceObjectiveName,* questo cmdlet restituisce i valori specificati e i predecessori.</span><span class="sxs-lookup"><span data-stu-id="e4948-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="e4948-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4948-110">EXAMPLES</span></span>

### <span data-ttu-id="e4948-111">Esempio 1: Ottenere funzionalità per l'abbonamento corrente per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="e4948-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="e4948-112">Questo comando restituisce le funzionalità per SQL istanze di database nella sottoscrizione corrente per l'area geografica Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="e4948-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="e4948-113">Esempio 2: Ottenere funzionalità predefinite per l'abbonamento corrente per un'area geografica</span><span class="sxs-lookup"><span data-stu-id="e4948-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="e4948-114">Questo comando restituisce le funzionalità predefinite per SQL database della sottoscrizione corrente nell'area centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="e4948-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="e4948-115">Esempio 3: Ottenere i dettagli per un obiettivo del servizio</span><span class="sxs-lookup"><span data-stu-id="e4948-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="e4948-116">Questo comando recupera le funzionalità predefinite per SQL database per l'obiettivo di servizio specificato nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e4948-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="e4948-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4948-117">PARAMETERS</span></span>

### <span data-ttu-id="e4948-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4948-118">-DefaultProfile</span></span>
<span data-ttu-id="e4948-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e4948-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4948-120">-Defaults</span><span class="sxs-lookup"><span data-stu-id="e4948-120">-Defaults</span></span>
<span data-ttu-id="e4948-121">Indica che questo cmdlet ottiene solo le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="e4948-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4948-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="e4948-122">-EditionName</span></span>
<span data-ttu-id="e4948-123">Specifica il nome dell'edizione del database per cui il cmdlet ottiene le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e4948-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4948-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="e4948-124">-LocationName</span></span>
<span data-ttu-id="e4948-125">Specifica il nome della posizione per cui il cmdlet ottiene funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e4948-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="e4948-126">Per altre informazioni, vedere Azure Regions http://azure.microsoft.com/en-us/regions/ ( http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="e4948-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="e4948-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="e4948-127">-ServerVersionName</span></span>
<span data-ttu-id="e4948-128">Specifica il nome della versione del server per cui il cmdlet ottiene le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e4948-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4948-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e4948-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="e4948-130">Specifica il nome dell'obiettivo del servizio per cui questo cmdlet ottiene funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e4948-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4948-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4948-131">-Confirm</span></span>
<span data-ttu-id="e4948-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4948-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4948-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4948-133">-WhatIf</span></span>
<span data-ttu-id="e4948-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4948-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4948-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4948-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4948-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4948-136">CommonParameters</span></span>
<span data-ttu-id="e4948-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4948-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4948-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4948-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4948-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4948-139">INPUTS</span></span>

### <span data-ttu-id="e4948-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e4948-140">System.String</span></span>

## <span data-ttu-id="e4948-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4948-141">OUTPUTS</span></span>

### <span data-ttu-id="e4948-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="e4948-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="e4948-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4948-143">NOTES</span></span>

## <span data-ttu-id="e4948-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4948-144">RELATED LINKS</span></span>
