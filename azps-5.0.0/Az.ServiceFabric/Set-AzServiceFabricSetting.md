---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 72a538c039914eebdcd2926cda93a97cfe2d267a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200992"
---
# <span data-ttu-id="9d2a1-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="9d2a1-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="9d2a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2a1-103">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="9d2a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d2a1-104">SYNTAX</span></span>

### <span data-ttu-id="9d2a1-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="9d2a1-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d2a1-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="9d2a1-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d2a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d2a1-107">DESCRIPTION</span></span>
<span data-ttu-id="9d2a1-108">Usare **set-AzServiceFabricSetting** per aggiungere o aggiornare le impostazioni del tessuto del servizio in un cluster.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="9d2a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d2a1-109">EXAMPLES</span></span>

### <span data-ttu-id="9d2a1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d2a1-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="9d2a1-111">Questo comando imposterà "MaxFileOperationTimeout" sul valore "5000" nella sezione "NamingService".</span><span class="sxs-lookup"><span data-stu-id="9d2a1-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="9d2a1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d2a1-112">PARAMETERS</span></span>

### <span data-ttu-id="9d2a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2a1-113">-DefaultProfile</span></span>
<span data-ttu-id="9d2a1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d2a1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d2a1-115">-Name</span></span>
<span data-ttu-id="9d2a1-116">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="9d2a1-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="9d2a1-117">Parametro-</span><span class="sxs-lookup"><span data-stu-id="9d2a1-117">-Parameter</span></span>
<span data-ttu-id="9d2a1-118">Nome parametro dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="9d2a1-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="9d2a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d2a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="9d2a1-120">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9d2a1-121">-Sezione</span><span class="sxs-lookup"><span data-stu-id="9d2a1-121">-Section</span></span>
<span data-ttu-id="9d2a1-122">Nome sezione dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="9d2a1-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="9d2a1-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="9d2a1-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="9d2a1-124">Matrice di impostazioni del tessuto</span><span class="sxs-lookup"><span data-stu-id="9d2a1-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="9d2a1-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="9d2a1-125">-Value</span></span>
<span data-ttu-id="9d2a1-126">Valore di parametro dell'impostazione del tessuto</span><span class="sxs-lookup"><span data-stu-id="9d2a1-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="9d2a1-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d2a1-127">-Confirm</span></span>
<span data-ttu-id="9d2a1-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d2a1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d2a1-129">-WhatIf</span></span>
<span data-ttu-id="9d2a1-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d2a1-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d2a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2a1-132">CommonParameters</span></span>
<span data-ttu-id="9d2a1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d2a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2a1-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d2a1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2a1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d2a1-135">INPUTS</span></span>

### <span data-ttu-id="9d2a1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9d2a1-136">System.String</span></span>

### <span data-ttu-id="9d2a1-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="9d2a1-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="9d2a1-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d2a1-138">OUTPUTS</span></span>

### <span data-ttu-id="9d2a1-139">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="9d2a1-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="9d2a1-140">Note</span><span class="sxs-lookup"><span data-stu-id="9d2a1-140">NOTES</span></span>

## <span data-ttu-id="9d2a1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d2a1-141">RELATED LINKS</span></span>
