---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: ac5e8bbc65a8435042d9f525cd1a3d35fa050398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014318"
---
# <span data-ttu-id="bff82-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bff82-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="bff82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff82-102">SYNOPSIS</span></span>
<span data-ttu-id="bff82-103">aggiornare una risorsa di Application Insights esistente</span><span class="sxs-lookup"><span data-stu-id="bff82-103">update an existing application insights resource</span></span>

## <span data-ttu-id="bff82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bff82-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bff82-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bff82-105">DESCRIPTION</span></span>
<span data-ttu-id="bff82-106">aggiornare una risorsa di Application Insights esistente</span><span class="sxs-lookup"><span data-stu-id="bff82-106">update an existing application insights resource</span></span>

## <span data-ttu-id="bff82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bff82-107">EXAMPLES</span></span>

### <span data-ttu-id="bff82-108">Esempio 1: Aggiornare il componente Application Insights</span><span class="sxs-lookup"><span data-stu-id="bff82-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="bff82-109">aggiornare il componente application insights "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery entrambi su "Disabled"</span><span class="sxs-lookup"><span data-stu-id="bff82-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="bff82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bff82-110">PARAMETERS</span></span>

### <span data-ttu-id="bff82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff82-111">-DefaultProfile</span></span>
<span data-ttu-id="bff82-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bff82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff82-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bff82-113">-Name</span></span>
<span data-ttu-id="bff82-114">Nome della risorsa Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bff82-114">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="bff82-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="bff82-116">Tipo di accesso di rete per l'accesso all'inserimento di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bff82-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="bff82-117">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="bff82-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="bff82-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="bff82-119">Tipo di accesso di rete per accedere alla query di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="bff82-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="bff82-120">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="bff82-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff82-121">-ResourceGroupName</span></span>
<span data-ttu-id="bff82-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bff82-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="bff82-123">-RetentionInDays</span></span>
<span data-ttu-id="bff82-124">Conservazione in giorni, 90 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bff82-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bff82-125">-Tag</span></span>
<span data-ttu-id="bff82-126">Contrassegni componenti.</span><span class="sxs-lookup"><span data-stu-id="bff82-126">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bff82-127">-Confirm</span></span>
<span data-ttu-id="bff82-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bff82-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff82-129">-WhatIf</span></span>
<span data-ttu-id="bff82-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bff82-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff82-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bff82-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff82-132">CommonParameters</span></span>
<span data-ttu-id="bff82-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff82-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bff82-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff82-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="bff82-135">INPUTS</span></span>

### <span data-ttu-id="bff82-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bff82-136">System.String</span></span>

## <span data-ttu-id="bff82-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bff82-137">OUTPUTS</span></span>

### <span data-ttu-id="bff82-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="bff82-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="bff82-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="bff82-139">NOTES</span></span>

## <span data-ttu-id="bff82-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bff82-140">RELATED LINKS</span></span>
