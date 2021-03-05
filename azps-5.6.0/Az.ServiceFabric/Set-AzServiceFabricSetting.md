---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: f98a5efeece2eb1e78479c3f76de62db495c6e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976333"
---
# <span data-ttu-id="ce286-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ce286-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="ce286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce286-102">SYNOPSIS</span></span>
<span data-ttu-id="ce286-103">Aggiungere o aggiornare una o più impostazioni di Service Fabric nel cluster.</span><span class="sxs-lookup"><span data-stu-id="ce286-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="ce286-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce286-104">SYNTAX</span></span>

### <span data-ttu-id="ce286-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="ce286-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce286-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="ce286-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce286-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce286-107">DESCRIPTION</span></span>
<span data-ttu-id="ce286-108">Usare **Set-AzServiceFabricSetting** per aggiungere o aggiornare le impostazioni di Service Fabric in un cluster.</span><span class="sxs-lookup"><span data-stu-id="ce286-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="ce286-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce286-109">EXAMPLES</span></span>

### <span data-ttu-id="ce286-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce286-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="ce286-111">Questo comando imposta 'MaxFileOperationTimeout' sul valore '5000' nella sezione 'NamingService'.</span><span class="sxs-lookup"><span data-stu-id="ce286-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="ce286-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ce286-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="ce286-113">Questo comando attiverà un aggiornamento per impostare più impostazioni di tessuto usando il parametro SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="ce286-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="ce286-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce286-114">PARAMETERS</span></span>

### <span data-ttu-id="ce286-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce286-115">-DefaultProfile</span></span>
<span data-ttu-id="ce286-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce286-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce286-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ce286-117">-Name</span></span>
<span data-ttu-id="ce286-118">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="ce286-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ce286-119">-Parameter</span></span>
<span data-ttu-id="ce286-120">Nome parametro dell'impostazione tessuto</span><span class="sxs-lookup"><span data-stu-id="ce286-120">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce286-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce286-122">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce286-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ce286-123">-Section</span><span class="sxs-lookup"><span data-stu-id="ce286-123">-Section</span></span>
<span data-ttu-id="ce286-124">Nome della sezione dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="ce286-124">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="ce286-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="ce286-126">Una serie di impostazioni dei tessuto</span><span class="sxs-lookup"><span data-stu-id="ce286-126">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-127">-Value</span><span class="sxs-lookup"><span data-stu-id="ce286-127">-Value</span></span>
<span data-ttu-id="ce286-128">Valore parametro dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="ce286-128">Parameter value of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce286-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce286-129">-Confirm</span></span>
<span data-ttu-id="ce286-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce286-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce286-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce286-131">-WhatIf</span></span>
<span data-ttu-id="ce286-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce286-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce286-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce286-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce286-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce286-134">CommonParameters</span></span>
<span data-ttu-id="ce286-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce286-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce286-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce286-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce286-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce286-137">INPUTS</span></span>

### <span data-ttu-id="ce286-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ce286-138">System.String</span></span>

### <span data-ttu-id="ce286-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="ce286-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="ce286-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce286-140">OUTPUTS</span></span>

### <span data-ttu-id="ce286-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="ce286-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ce286-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce286-142">NOTES</span></span>

## <span data-ttu-id="ce286-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce286-143">RELATED LINKS</span></span>
