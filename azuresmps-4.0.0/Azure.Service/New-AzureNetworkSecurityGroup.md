---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023868"
---
# <span data-ttu-id="f3afb-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f3afb-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="f3afb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3afb-102">SYNOPSIS</span></span>
<span data-ttu-id="f3afb-103">Crea un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="f3afb-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="f3afb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3afb-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3afb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3afb-105">DESCRIPTION</span></span>
<span data-ttu-id="f3afb-106">Il cmdlet **New-AzureNetworkSecurityGroup** crea un gruppo di sicurezza di rete Azure in una posizione.</span><span class="sxs-lookup"><span data-stu-id="f3afb-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="f3afb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3afb-107">EXAMPLES</span></span>

## <span data-ttu-id="f3afb-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3afb-108">PARAMETERS</span></span>

### <span data-ttu-id="f3afb-109">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="f3afb-109">-Label</span></span>
<span data-ttu-id="f3afb-110">Specifica una descrizione per il nuovo gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="f3afb-110">Specifies a description for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3afb-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f3afb-111">-Location</span></span>
<span data-ttu-id="f3afb-112">Specifica la posizione di Azure in cui questo cmdlet crea un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="f3afb-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="f3afb-113">Per ottenere posizioni valide, usare il cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="f3afb-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3afb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3afb-114">-Name</span></span>
<span data-ttu-id="f3afb-115">Specifica un nome per il nuovo gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="f3afb-115">Specifies a name for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3afb-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="f3afb-116">-Profile</span></span>
<span data-ttu-id="f3afb-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3afb-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f3afb-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f3afb-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3afb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3afb-119">CommonParameters</span></span>
<span data-ttu-id="f3afb-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3afb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3afb-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3afb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3afb-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3afb-122">INPUTS</span></span>

## <span data-ttu-id="f3afb-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3afb-123">OUTPUTS</span></span>

## <span data-ttu-id="f3afb-124">Note</span><span class="sxs-lookup"><span data-stu-id="f3afb-124">NOTES</span></span>

## <span data-ttu-id="f3afb-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3afb-125">RELATED LINKS</span></span>

[<span data-ttu-id="f3afb-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f3afb-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


