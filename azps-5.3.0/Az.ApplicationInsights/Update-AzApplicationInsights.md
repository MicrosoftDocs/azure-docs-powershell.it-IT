---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381205"
---
# <span data-ttu-id="176df-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="176df-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="176df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="176df-102">SYNOPSIS</span></span>
<span data-ttu-id="176df-103">aggiornare una risorsa approfondimenti applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="176df-103">update an existing application insights resource</span></span>

## <span data-ttu-id="176df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="176df-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="176df-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="176df-105">DESCRIPTION</span></span>
<span data-ttu-id="176df-106">aggiornare una risorsa approfondimenti applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="176df-106">update an existing application insights resource</span></span>

## <span data-ttu-id="176df-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="176df-107">EXAMPLES</span></span>

### <span data-ttu-id="176df-108">Esempio 1 componente approfondimenti dell'applicazione di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="176df-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="176df-109">aggiornare il componente Insights applicazione "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery sia per "disabled"</span><span class="sxs-lookup"><span data-stu-id="176df-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="176df-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="176df-110">PARAMETERS</span></span>

### <span data-ttu-id="176df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176df-111">-DefaultProfile</span></span>
<span data-ttu-id="176df-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="176df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176df-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="176df-113">-Name</span></span>
<span data-ttu-id="176df-114">Nome risorsa informazioni approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="176df-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="176df-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="176df-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="176df-116">Tipo di accesso alla rete per l'accesso all'ingestione di Insight per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="176df-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="176df-117">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="176df-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="176df-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="176df-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="176df-119">Tipo di accesso alla rete per l'accesso alla query Insights dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="176df-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="176df-120">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="176df-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="176df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176df-121">-ResourceGroupName</span></span>
<span data-ttu-id="176df-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="176df-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="176df-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="176df-123">-RetentionInDays</span></span>
<span data-ttu-id="176df-124">Conservazione in giorni, 90 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="176df-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="176df-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="176df-125">-Tag</span></span>
<span data-ttu-id="176df-126">Tag del componente.</span><span class="sxs-lookup"><span data-stu-id="176df-126">Component Tags.</span></span>

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

### <span data-ttu-id="176df-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="176df-127">-Confirm</span></span>
<span data-ttu-id="176df-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176df-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176df-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176df-129">-WhatIf</span></span>
<span data-ttu-id="176df-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="176df-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176df-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="176df-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176df-132">CommonParameters</span></span>
<span data-ttu-id="176df-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176df-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="176df-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176df-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="176df-135">INPUTS</span></span>

### <span data-ttu-id="176df-136">System. String</span><span class="sxs-lookup"><span data-stu-id="176df-136">System.String</span></span>

## <span data-ttu-id="176df-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="176df-137">OUTPUTS</span></span>

### <span data-ttu-id="176df-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="176df-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="176df-139">Note</span><span class="sxs-lookup"><span data-stu-id="176df-139">NOTES</span></span>

## <span data-ttu-id="176df-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="176df-140">RELATED LINKS</span></span>
