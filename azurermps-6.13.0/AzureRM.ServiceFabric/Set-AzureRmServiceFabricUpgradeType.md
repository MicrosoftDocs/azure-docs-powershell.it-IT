---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: ddab39c3ad575cd46c427c7346fd635217c0dbca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516448"
---
# <span data-ttu-id="8447e-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="8447e-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="8447e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8447e-102">SYNOPSIS</span></span>
<span data-ttu-id="8447e-103">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="8447e-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8447e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8447e-104">SYNTAX</span></span>

### <span data-ttu-id="8447e-105">Automatico</span><span class="sxs-lookup"><span data-stu-id="8447e-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8447e-106">Manuale</span><span class="sxs-lookup"><span data-stu-id="8447e-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8447e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8447e-107">DESCRIPTION</span></span>
<span data-ttu-id="8447e-108">Usare **set-AzureRmServiceFabricUpgradeType** per impostare il tipo di aggiornamento su automatico o manuale con una versione specifica del codice del tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="8447e-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="8447e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8447e-109">EXAMPLES</span></span>

### <span data-ttu-id="8447e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8447e-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="8447e-111">Questo comando consentirà di impostare la modalità di aggiornamento del cluster su automatica.</span><span class="sxs-lookup"><span data-stu-id="8447e-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="8447e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8447e-112">PARAMETERS</span></span>

### <span data-ttu-id="8447e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8447e-113">-DefaultProfile</span></span>
<span data-ttu-id="8447e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8447e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8447e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8447e-115">-Name</span></span>
<span data-ttu-id="8447e-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="8447e-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8447e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8447e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8447e-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8447e-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8447e-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8447e-119">-UpgradeMode</span></span>
<span data-ttu-id="8447e-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8447e-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8447e-121">-Versione</span><span class="sxs-lookup"><span data-stu-id="8447e-121">-Version</span></span>
<span data-ttu-id="8447e-122">Versione del codice del cluster.</span><span class="sxs-lookup"><span data-stu-id="8447e-122">Cluster code version.</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8447e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8447e-123">-Confirm</span></span>
<span data-ttu-id="8447e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8447e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8447e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8447e-125">-WhatIf</span></span>
<span data-ttu-id="8447e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8447e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8447e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8447e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8447e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8447e-128">CommonParameters</span></span>
<span data-ttu-id="8447e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8447e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8447e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8447e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8447e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8447e-131">INPUTS</span></span>

### <span data-ttu-id="8447e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8447e-132">System.String</span></span>
<span data-ttu-id="8447e-133">Parametri: versione (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8447e-133">Parameters: Version (ByValue)</span></span>

### <span data-ttu-id="8447e-134">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8447e-134">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="8447e-135">Parametri: UpgradeMode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8447e-135">Parameters: UpgradeMode (ByValue)</span></span>

## <span data-ttu-id="8447e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8447e-136">OUTPUTS</span></span>

### <span data-ttu-id="8447e-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="8447e-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8447e-138">Note</span><span class="sxs-lookup"><span data-stu-id="8447e-138">NOTES</span></span>

## <span data-ttu-id="8447e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8447e-139">RELATED LINKS</span></span>
