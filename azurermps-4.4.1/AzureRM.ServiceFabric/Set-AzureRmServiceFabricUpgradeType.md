---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 7884e45c2b4f635c9236f213a93eb69524b37fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685867"
---
# <span data-ttu-id="2468b-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2468b-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="2468b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2468b-102">SYNOPSIS</span></span>
<span data-ttu-id="2468b-103">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="2468b-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2468b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2468b-104">SYNTAX</span></span>

### <span data-ttu-id="2468b-105">Automatico</span><span class="sxs-lookup"><span data-stu-id="2468b-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2468b-106">Manuale</span><span class="sxs-lookup"><span data-stu-id="2468b-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2468b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2468b-107">DESCRIPTION</span></span>
<span data-ttu-id="2468b-108">Usare **set-AzureRmServiceFabricUpgradeType** per impostare il tipo di aggiornamento su automatico o manuale con una versione specifica del codice del tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="2468b-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="2468b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2468b-109">EXAMPLES</span></span>

### <span data-ttu-id="2468b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2468b-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="2468b-111">Questo comando consentirà di impostare la modalità di aggiornamento del cluster su automatica.</span><span class="sxs-lookup"><span data-stu-id="2468b-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="2468b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2468b-112">PARAMETERS</span></span>

### <span data-ttu-id="2468b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2468b-113">-Name</span></span>
<span data-ttu-id="2468b-114">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="2468b-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2468b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2468b-115">-ResourceGroupName</span></span>
<span data-ttu-id="2468b-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2468b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2468b-117">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="2468b-117">-UpgradeMode</span></span>
<span data-ttu-id="2468b-118">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="2468b-118">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="2468b-119">-Versione</span><span class="sxs-lookup"><span data-stu-id="2468b-119">-Version</span></span>
<span data-ttu-id="2468b-120">Versione del codice del cluster.</span><span class="sxs-lookup"><span data-stu-id="2468b-120">Cluster code version.</span></span>

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

### <span data-ttu-id="2468b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2468b-121">-Confirm</span></span>
<span data-ttu-id="2468b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2468b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2468b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2468b-123">-WhatIf</span></span>
<span data-ttu-id="2468b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2468b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2468b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2468b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2468b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2468b-126">-DefaultProfile</span></span>
<span data-ttu-id="2468b-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2468b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2468b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2468b-128">CommonParameters</span></span>
<span data-ttu-id="2468b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2468b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2468b-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2468b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2468b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2468b-131">INPUTS</span></span>

### <span data-ttu-id="2468b-132">Microsoft. Azure. Commands. ServiceFabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="2468b-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="2468b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2468b-133">System.String</span></span>

## <span data-ttu-id="2468b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2468b-134">OUTPUTS</span></span>

### <span data-ttu-id="2468b-135">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="2468b-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="2468b-136">Note</span><span class="sxs-lookup"><span data-stu-id="2468b-136">NOTES</span></span>

## <span data-ttu-id="2468b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2468b-137">RELATED LINKS</span></span>

