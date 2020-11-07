---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860754"
---
# <span data-ttu-id="5f11b-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f11b-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="5f11b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f11b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f11b-103">Ottiene un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="5f11b-103">Gets a network security group.</span></span>

## <span data-ttu-id="5f11b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f11b-104">SYNTAX</span></span>

### <span data-ttu-id="5f11b-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="5f11b-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f11b-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="5f11b-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f11b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f11b-107">DESCRIPTION</span></span>
<span data-ttu-id="5f11b-108">Il cmdlet **Get-AzNetworkSecurityGroup** ottiene un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="5f11b-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="5f11b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f11b-109">EXAMPLES</span></span>

### <span data-ttu-id="5f11b-110">1: recuperare un gruppo di sicurezza di rete esistente</span><span class="sxs-lookup"><span data-stu-id="5f11b-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="5f11b-111">Questo comando restituisce il contenuto del gruppo di sicurezza di rete Azure "nsg1" nel gruppo di risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="5f11b-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="5f11b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f11b-112">PARAMETERS</span></span>

### <span data-ttu-id="5f11b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f11b-113">-DefaultProfile</span></span>
<span data-ttu-id="5f11b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f11b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f11b-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5f11b-115">-ExpandResource</span></span>
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

### <span data-ttu-id="5f11b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f11b-116">-Name</span></span>
<span data-ttu-id="5f11b-117">Specifica il nome del gruppo di sicurezza di rete ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f11b-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f11b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f11b-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f11b-119">Specifica il nome del gruppo di risorse a cui appartiene il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="5f11b-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="5f11b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f11b-120">CommonParameters</span></span>
<span data-ttu-id="5f11b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f11b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f11b-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f11b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f11b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f11b-123">INPUTS</span></span>

## <span data-ttu-id="5f11b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f11b-124">OUTPUTS</span></span>

### <span data-ttu-id="5f11b-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f11b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5f11b-126">Note</span><span class="sxs-lookup"><span data-stu-id="5f11b-126">NOTES</span></span>

## <span data-ttu-id="5f11b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f11b-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f11b-128">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f11b-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5f11b-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f11b-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5f11b-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f11b-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


