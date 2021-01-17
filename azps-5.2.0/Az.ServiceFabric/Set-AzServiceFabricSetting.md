---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362470"
---
# <span data-ttu-id="1e5e2-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1e5e2-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="1e5e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e5e2-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5e2-103">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="1e5e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e5e2-104">SYNTAX</span></span>

### <span data-ttu-id="1e5e2-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="1e5e2-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e5e2-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="1e5e2-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e5e2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e5e2-107">DESCRIPTION</span></span>
<span data-ttu-id="1e5e2-108">Usare **set-AzServiceFabricSetting** per aggiungere o aggiornare le impostazioni del tessuto del servizio in un cluster.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="1e5e2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e5e2-109">EXAMPLES</span></span>

### <span data-ttu-id="1e5e2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e5e2-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="1e5e2-111">Questo comando imposterà "MaxFileOperationTimeout" sul valore "5000" nella sezione "NamingService".</span><span class="sxs-lookup"><span data-stu-id="1e5e2-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="1e5e2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1e5e2-112">Example 2</span></span>
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

<span data-ttu-id="1e5e2-113">Questo comando attiverà un aggiornamento per impostare l'impostazione di più fabric usando il parametro SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="1e5e2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e5e2-114">PARAMETERS</span></span>

### <span data-ttu-id="1e5e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5e2-115">-DefaultProfile</span></span>
<span data-ttu-id="1e5e2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e5e2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e5e2-117">-Name</span></span>
<span data-ttu-id="1e5e2-118">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="1e5e2-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="1e5e2-119">Parametro-</span><span class="sxs-lookup"><span data-stu-id="1e5e2-119">-Parameter</span></span>
<span data-ttu-id="1e5e2-120">Nome parametro dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="1e5e2-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="1e5e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="1e5e2-122">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1e5e2-123">-Sezione</span><span class="sxs-lookup"><span data-stu-id="1e5e2-123">-Section</span></span>
<span data-ttu-id="1e5e2-124">Nome sezione dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="1e5e2-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="1e5e2-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="1e5e2-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="1e5e2-126">Matrice di impostazioni del tessuto</span><span class="sxs-lookup"><span data-stu-id="1e5e2-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="1e5e2-127">-Valore</span><span class="sxs-lookup"><span data-stu-id="1e5e2-127">-Value</span></span>
<span data-ttu-id="1e5e2-128">Valore di parametro dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="1e5e2-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="1e5e2-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e5e2-129">-Confirm</span></span>
<span data-ttu-id="1e5e2-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e5e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5e2-131">-WhatIf</span></span>
<span data-ttu-id="1e5e2-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5e2-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e5e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5e2-134">CommonParameters</span></span>
<span data-ttu-id="1e5e2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5e2-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e5e2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5e2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e5e2-137">INPUTS</span></span>

### <span data-ttu-id="1e5e2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1e5e2-138">System.String</span></span>

### <span data-ttu-id="1e5e2-139">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="1e5e2-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="1e5e2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e5e2-140">OUTPUTS</span></span>

### <span data-ttu-id="1e5e2-141">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="1e5e2-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1e5e2-142">Note</span><span class="sxs-lookup"><span data-stu-id="1e5e2-142">NOTES</span></span>

## <span data-ttu-id="1e5e2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e5e2-143">RELATED LINKS</span></span>
