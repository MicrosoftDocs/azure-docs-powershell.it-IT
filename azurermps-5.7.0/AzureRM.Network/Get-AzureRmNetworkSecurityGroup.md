---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: dc9934aaee7706e3577039bdb77c5a6a54c29c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519427"
---
# <span data-ttu-id="4408c-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4408c-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="4408c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4408c-102">SYNOPSIS</span></span>
<span data-ttu-id="4408c-103">Ottiene un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="4408c-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4408c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4408c-104">SYNTAX</span></span>

### <span data-ttu-id="4408c-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="4408c-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4408c-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="4408c-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4408c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4408c-107">DESCRIPTION</span></span>
<span data-ttu-id="4408c-108">Il cmdlet **Get-AzureRmNetworkSecurityGroup** ottiene un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="4408c-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="4408c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4408c-109">EXAMPLES</span></span>

### <span data-ttu-id="4408c-110">1: recuperare un gruppo di sicurezza di rete esistente</span><span class="sxs-lookup"><span data-stu-id="4408c-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="4408c-111">Questo comando restituisce il contenuto del gruppo di sicurezza di rete Azure "nsg1" nel gruppo di risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="4408c-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="4408c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4408c-112">PARAMETERS</span></span>

### <span data-ttu-id="4408c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4408c-113">-DefaultProfile</span></span>
<span data-ttu-id="4408c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4408c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4408c-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4408c-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4408c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4408c-116">-Name</span></span>
<span data-ttu-id="4408c-117">Specifica il nome del gruppo di sicurezza di rete ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4408c-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4408c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4408c-118">-ResourceGroupName</span></span>
<span data-ttu-id="4408c-119">Specifica il nome del gruppo di risorse a cui appartiene il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="4408c-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4408c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4408c-120">CommonParameters</span></span>
<span data-ttu-id="4408c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4408c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4408c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4408c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4408c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4408c-123">INPUTS</span></span>

### <span data-ttu-id="4408c-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4408c-124">None</span></span>
<span data-ttu-id="4408c-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4408c-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4408c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4408c-126">OUTPUTS</span></span>

### <span data-ttu-id="4408c-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4408c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4408c-128">Note</span><span class="sxs-lookup"><span data-stu-id="4408c-128">NOTES</span></span>

## <span data-ttu-id="4408c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4408c-129">RELATED LINKS</span></span>

[<span data-ttu-id="4408c-130">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4408c-130">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="4408c-131">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4408c-131">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="4408c-132">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4408c-132">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


