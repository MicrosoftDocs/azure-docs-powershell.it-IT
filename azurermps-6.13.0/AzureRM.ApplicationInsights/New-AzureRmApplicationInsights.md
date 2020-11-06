---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 48922d3e0cbf8cf322d25657c76ee01e0ee238b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509388"
---
# <span data-ttu-id="f0d4a-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f0d4a-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="f0d4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d4a-103">Creare una nuova risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="f0d4a-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0d4a-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0d4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d4a-106">Creare una nuova risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="f0d4a-106">Create a new application insights resource</span></span>

## <span data-ttu-id="f0d4a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="f0d4a-108">Esempio 1 creare una nuova risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="f0d4a-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
```

<span data-ttu-id="f0d4a-109">Aggiungere una nuova risorsa approfondimenti applicazione denominata "test" nel gruppo risorse "testgroup" con il tipo "Java".</span><span class="sxs-lookup"><span data-stu-id="f0d4a-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="f0d4a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0d4a-110">PARAMETERS</span></span>

### <span data-ttu-id="f0d4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d4a-111">-DefaultProfile</span></span>
<span data-ttu-id="f0d4a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d4a-113">-Tipo</span><span class="sxs-lookup"><span data-stu-id="f0d4a-113">-Kind</span></span>
<span data-ttu-id="f0d4a-114">Tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d4a-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f0d4a-115">-Location</span></span>
<span data-ttu-id="f0d4a-116">Percorso delle risorse dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d4a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0d4a-117">-Name</span></span>
<span data-ttu-id="f0d4a-118">Nome risorsa informazioni approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="f0d4a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d4a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0d4a-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0d4a-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0d4a-121">-Tag</span></span>
<span data-ttu-id="f0d4a-122">Tag del componente.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-122">Component Tags.</span></span>

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

### <span data-ttu-id="f0d4a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0d4a-123">-Confirm</span></span>
<span data-ttu-id="f0d4a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d4a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d4a-125">-WhatIf</span></span>
<span data-ttu-id="f0d4a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0d4a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d4a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d4a-128">CommonParameters</span></span>
<span data-ttu-id="f0d4a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d4a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d4a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d4a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d4a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0d4a-131">INPUTS</span></span>

### <span data-ttu-id="f0d4a-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0d4a-132">None</span></span>

## <span data-ttu-id="f0d4a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0d4a-133">OUTPUTS</span></span>

### <span data-ttu-id="f0d4a-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f0d4a-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="f0d4a-135">Note</span><span class="sxs-lookup"><span data-stu-id="f0d4a-135">NOTES</span></span>

## <span data-ttu-id="f0d4a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0d4a-136">RELATED LINKS</span></span>
