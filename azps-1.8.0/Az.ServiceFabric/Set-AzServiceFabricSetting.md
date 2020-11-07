---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: cea8ec21021725bae99ef597a33079621f539cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677061"
---
# <span data-ttu-id="694e3-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="694e3-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="694e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="694e3-102">SYNOPSIS</span></span>
<span data-ttu-id="694e3-103">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="694e3-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="694e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="694e3-104">SYNTAX</span></span>

### <span data-ttu-id="694e3-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="694e3-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="694e3-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="694e3-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="694e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="694e3-107">DESCRIPTION</span></span>
<span data-ttu-id="694e3-108">Usare **set-AzServiceFabricSetting** per aggiungere o aggiornare le impostazioni del tessuto del servizio in un cluster.</span><span class="sxs-lookup"><span data-stu-id="694e3-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="694e3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="694e3-109">EXAMPLES</span></span>

### <span data-ttu-id="694e3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="694e3-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="694e3-111">Questo comando imposterà "MaxFileOperationTimeout" sul valore "5000" nella sezione "NamingService".</span><span class="sxs-lookup"><span data-stu-id="694e3-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="694e3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="694e3-112">PARAMETERS</span></span>

### <span data-ttu-id="694e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694e3-113">-DefaultProfile</span></span>
<span data-ttu-id="694e3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="694e3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="694e3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="694e3-115">-Name</span></span>
<span data-ttu-id="694e3-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="694e3-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="694e3-117">Parametro-</span><span class="sxs-lookup"><span data-stu-id="694e3-117">-Parameter</span></span>
<span data-ttu-id="694e3-118">Parametro.</span><span class="sxs-lookup"><span data-stu-id="694e3-118">Parameter.</span></span>

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

### <span data-ttu-id="694e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="694e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="694e3-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="694e3-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="694e3-121">-Sezione</span><span class="sxs-lookup"><span data-stu-id="694e3-121">-Section</span></span>
<span data-ttu-id="694e3-122">Sezione.</span><span class="sxs-lookup"><span data-stu-id="694e3-122">Section.</span></span>

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

### <span data-ttu-id="694e3-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="694e3-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="694e3-124">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="694e3-124">Client authentication type.</span></span>

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

### <span data-ttu-id="694e3-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="694e3-125">-Value</span></span>
<span data-ttu-id="694e3-126">Valore.</span><span class="sxs-lookup"><span data-stu-id="694e3-126">Value.</span></span>

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

### <span data-ttu-id="694e3-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="694e3-127">-Confirm</span></span>
<span data-ttu-id="694e3-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="694e3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="694e3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="694e3-129">-WhatIf</span></span>
<span data-ttu-id="694e3-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="694e3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="694e3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="694e3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="694e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694e3-132">CommonParameters</span></span>
<span data-ttu-id="694e3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="694e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694e3-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694e3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694e3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="694e3-135">INPUTS</span></span>

### <span data-ttu-id="694e3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="694e3-136">System.String</span></span>

### <span data-ttu-id="694e3-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="694e3-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="694e3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="694e3-138">OUTPUTS</span></span>

### <span data-ttu-id="694e3-139">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="694e3-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="694e3-140">Note</span><span class="sxs-lookup"><span data-stu-id="694e3-140">NOTES</span></span>

## <span data-ttu-id="694e3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="694e3-141">RELATED LINKS</span></span>
