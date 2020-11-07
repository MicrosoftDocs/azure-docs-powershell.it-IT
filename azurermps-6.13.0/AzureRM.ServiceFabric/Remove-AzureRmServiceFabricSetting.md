---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 4643ab29be9c93f58895048317edc2b1db6115e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687577"
---
# <span data-ttu-id="0d23f-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0d23f-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="0d23f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d23f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d23f-103">Rimuovere una o più impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="0d23f-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d23f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d23f-104">SYNTAX</span></span>

### <span data-ttu-id="0d23f-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="0d23f-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d23f-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="0d23f-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d23f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d23f-107">DESCRIPTION</span></span>
<span data-ttu-id="0d23f-108">Usare **Remove-AzureRmServiceFabricSetting** per rimuovere le impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="0d23f-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="0d23f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d23f-109">EXAMPLES</span></span>

### <span data-ttu-id="0d23f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d23f-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="0d23f-111">Questo comando rimuove le impostazioni "MaxCursors" nella sezione "EseStore".</span><span class="sxs-lookup"><span data-stu-id="0d23f-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="0d23f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d23f-112">PARAMETERS</span></span>

### <span data-ttu-id="0d23f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d23f-113">-DefaultProfile</span></span>
<span data-ttu-id="0d23f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d23f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d23f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d23f-115">-Name</span></span>
<span data-ttu-id="0d23f-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0d23f-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0d23f-117">Parametro-</span><span class="sxs-lookup"><span data-stu-id="0d23f-117">-Parameter</span></span>
<span data-ttu-id="0d23f-118">Parametro.</span><span class="sxs-lookup"><span data-stu-id="0d23f-118">Parameter.</span></span>

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

### <span data-ttu-id="0d23f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d23f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d23f-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d23f-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0d23f-121">-Sezione</span><span class="sxs-lookup"><span data-stu-id="0d23f-121">-Section</span></span>
<span data-ttu-id="0d23f-122">Sezione.</span><span class="sxs-lookup"><span data-stu-id="0d23f-122">Section.</span></span>

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

### <span data-ttu-id="0d23f-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="0d23f-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="0d23f-124">Tipo di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="0d23f-124">Client authentication type.</span></span>

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

### <span data-ttu-id="0d23f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d23f-125">-Confirm</span></span>
<span data-ttu-id="0d23f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d23f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d23f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d23f-127">-WhatIf</span></span>
<span data-ttu-id="0d23f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d23f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d23f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d23f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d23f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d23f-130">CommonParameters</span></span>
<span data-ttu-id="0d23f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d23f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d23f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d23f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d23f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d23f-133">INPUTS</span></span>

### <span data-ttu-id="0d23f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0d23f-134">System.String</span></span>
<span data-ttu-id="0d23f-135">Parameters: Parameter (ByValue), Section (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d23f-135">Parameters: Parameter (ByValue), Section (ByValue)</span></span>

### <span data-ttu-id="0d23f-136">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="0d23f-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="0d23f-137">Parametri: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d23f-137">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="0d23f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d23f-138">OUTPUTS</span></span>

### <span data-ttu-id="0d23f-139">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0d23f-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0d23f-140">Note</span><span class="sxs-lookup"><span data-stu-id="0d23f-140">NOTES</span></span>

## <span data-ttu-id="0d23f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d23f-141">RELATED LINKS</span></span>
