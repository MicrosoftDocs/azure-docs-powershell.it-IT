---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688555"
---
# <span data-ttu-id="70f6a-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="70f6a-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="70f6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="70f6a-103">Ottiene una risorsa di configurazione tap.</span><span class="sxs-lookup"><span data-stu-id="70f6a-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70f6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70f6a-104">SYNTAX</span></span>

### <span data-ttu-id="70f6a-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70f6a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f6a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70f6a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70f6a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70f6a-107">DESCRIPTION</span></span>
<span data-ttu-id="70f6a-108">Il cmdlet **Get-AzureRmNetworkInterfaceTapConfig** ottiene una configurazione di Azure tap per un gruppo di risorse specifico, un'interfaccia di rete e un nome di configurazione di tocco o un elenco di configurazioni di tocco in un gruppo di risorse e in un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="70f6a-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="70f6a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70f6a-109">EXAMPLES</span></span>

### <span data-ttu-id="70f6a-110">Esempio 1: ottenere tutte le configurazioni di tocco per una determinata interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="70f6a-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="70f6a-111">Questo comando ottiene il tocco delle configurazioni aggiunte per l'interfaccia di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="70f6a-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="70f6a-112">Esempio 2: ottenere una configurazione di tocco specificata</span><span class="sxs-lookup"><span data-stu-id="70f6a-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="70f6a-113">Con questo comando viene aggiunta una configurazione di tocco specifica per l'interfaccia di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="70f6a-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="70f6a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70f6a-114">PARAMETERS</span></span>

### <span data-ttu-id="70f6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f6a-115">-DefaultProfile</span></span>
<span data-ttu-id="70f6a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70f6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70f6a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="70f6a-117">-Name</span></span>
<span data-ttu-id="70f6a-118">Nome della configurazione del tocco specifico.</span><span class="sxs-lookup"><span data-stu-id="70f6a-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f6a-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="70f6a-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="70f6a-120">Nome dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="70f6a-120">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f6a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f6a-121">-ResourceGroupName</span></span>
<span data-ttu-id="70f6a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70f6a-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f6a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70f6a-123">-ResourceId</span></span>
<span data-ttu-id="70f6a-124">ResourceId della risorsa TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="70f6a-124">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f6a-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="70f6a-125">-Confirm</span></span>
<span data-ttu-id="70f6a-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70f6a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f6a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f6a-127">-WhatIf</span></span>
<span data-ttu-id="70f6a-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70f6a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70f6a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70f6a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70f6a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f6a-130">CommonParameters</span></span>
<span data-ttu-id="70f6a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f6a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f6a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f6a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f6a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70f6a-133">INPUTS</span></span>

### <span data-ttu-id="70f6a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="70f6a-134">System.String</span></span>

## <span data-ttu-id="70f6a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70f6a-135">OUTPUTS</span></span>

### <span data-ttu-id="70f6a-136">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="70f6a-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="70f6a-137">Note</span><span class="sxs-lookup"><span data-stu-id="70f6a-137">NOTES</span></span>

## <span data-ttu-id="70f6a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70f6a-138">RELATED LINKS</span></span>