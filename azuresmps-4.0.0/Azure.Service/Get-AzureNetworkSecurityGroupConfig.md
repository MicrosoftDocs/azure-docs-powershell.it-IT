---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029795"
---
# <span data-ttu-id="9902e-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="9902e-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="9902e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9902e-102">SYNOPSIS</span></span>
<span data-ttu-id="9902e-103">Ottiene i dettagli per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="9902e-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="9902e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9902e-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9902e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9902e-105">DESCRIPTION</span></span>
<span data-ttu-id="9902e-106">Il cmdlet **Get-AzureNetworkSecurityGroupConfig** restituisce i dettagli per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="9902e-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="9902e-107">Specificare il parametro *dettagliato* per visualizzare le regole di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="9902e-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="9902e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9902e-108">EXAMPLES</span></span>

## <span data-ttu-id="9902e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9902e-109">PARAMETERS</span></span>

### <span data-ttu-id="9902e-110">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="9902e-110">-Detailed</span></span>
<span data-ttu-id="9902e-111">Indica che questo cmdlet Visualizza le regole di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="9902e-111">Indicates that this cmdlet displays the network security rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9902e-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="9902e-112">-Profile</span></span>
<span data-ttu-id="9902e-113">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9902e-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9902e-114">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9902e-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9902e-115">-VM</span><span class="sxs-lookup"><span data-stu-id="9902e-115">-VM</span></span>
<span data-ttu-id="9902e-116">Specifica la macchina virtuale per cui questo cmdlet ottiene i dettagli di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="9902e-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9902e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9902e-117">CommonParameters</span></span>
<span data-ttu-id="9902e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9902e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9902e-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9902e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9902e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9902e-120">INPUTS</span></span>

## <span data-ttu-id="9902e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9902e-121">OUTPUTS</span></span>

## <span data-ttu-id="9902e-122">Note</span><span class="sxs-lookup"><span data-stu-id="9902e-122">NOTES</span></span>

## <span data-ttu-id="9902e-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9902e-123">RELATED LINKS</span></span>

[<span data-ttu-id="9902e-124">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9902e-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="9902e-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9902e-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


