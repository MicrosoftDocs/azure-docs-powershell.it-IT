---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030032"
---
# <span data-ttu-id="31b09-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="31b09-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="31b09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31b09-102">SYNOPSIS</span></span>
<span data-ttu-id="31b09-103">Recupera informazioni sulle reti virtuali di Azure RemoteApp in Azure.</span><span class="sxs-lookup"><span data-stu-id="31b09-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="31b09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b09-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="31b09-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31b09-105">DESCRIPTION</span></span>
<span data-ttu-id="31b09-106">Il cmdlet **Get-AzureRemoteAppVNet** recupera informazioni sulle reti virtuali di Azure RemoteApp in Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="31b09-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="31b09-107">Questo cmdlet restituisce un oggetto che contiene informazioni su una rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="31b09-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="31b09-108">Se non viene specificata una rete virtuale, questo cmdlet restituisce informazioni su tutte le reti virtuali dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="31b09-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="31b09-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b09-109">EXAMPLES</span></span>

### <span data-ttu-id="31b09-110">Esempio 1: recuperare informazioni su una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="31b09-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="31b09-111">Questo comando consente di ottenere informazioni sulla rete virtuale denominata ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="31b09-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="31b09-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31b09-112">PARAMETERS</span></span>

### <span data-ttu-id="31b09-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="31b09-113">-IncludeSharedKey</span></span>
<span data-ttu-id="31b09-114">Indica che questo cmdlet include il valore della chiave condivisa nelle informazioni recuperate sulla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="31b09-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

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

### <span data-ttu-id="31b09-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="31b09-115">-Profile</span></span>
<span data-ttu-id="31b09-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31b09-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31b09-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="31b09-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31b09-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="31b09-118">-VNetName</span></span>
<span data-ttu-id="31b09-119">Specifica il nome della rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="31b09-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="31b09-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b09-120">CommonParameters</span></span>
<span data-ttu-id="31b09-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b09-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b09-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b09-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b09-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31b09-123">INPUTS</span></span>

## <span data-ttu-id="31b09-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b09-124">OUTPUTS</span></span>

## <span data-ttu-id="31b09-125">Note</span><span class="sxs-lookup"><span data-stu-id="31b09-125">NOTES</span></span>

## <span data-ttu-id="31b09-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b09-126">RELATED LINKS</span></span>

[<span data-ttu-id="31b09-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="31b09-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


