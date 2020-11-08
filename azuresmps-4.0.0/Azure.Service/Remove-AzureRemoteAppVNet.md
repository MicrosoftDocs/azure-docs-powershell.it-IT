---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029608"
---
# <span data-ttu-id="66859-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="66859-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="66859-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66859-102">SYNOPSIS</span></span>
<span data-ttu-id="66859-103">Elimina una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="66859-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="66859-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66859-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66859-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66859-105">DESCRIPTION</span></span>
<span data-ttu-id="66859-106">Il cmdlet **Remove-AzureRemoteAppVNet** Elimina una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="66859-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="66859-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66859-107">EXAMPLES</span></span>

### <span data-ttu-id="66859-108">Esempio 1: eliminare una rete virtuale specificata</span><span class="sxs-lookup"><span data-stu-id="66859-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="66859-109">Questo comando Elimina la rete virtuale denominata ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="66859-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="66859-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66859-110">PARAMETERS</span></span>

### <span data-ttu-id="66859-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="66859-111">-Profile</span></span>
<span data-ttu-id="66859-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66859-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66859-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="66859-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66859-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="66859-114">-VNetName</span></span>
<span data-ttu-id="66859-115">Specifica il nome della rete virtuale di Azure RemoteApp da eliminare.</span><span class="sxs-lookup"><span data-stu-id="66859-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66859-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66859-116">CommonParameters</span></span>
<span data-ttu-id="66859-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66859-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66859-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66859-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66859-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66859-119">INPUTS</span></span>

## <span data-ttu-id="66859-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66859-120">OUTPUTS</span></span>

## <span data-ttu-id="66859-121">Note</span><span class="sxs-lookup"><span data-stu-id="66859-121">NOTES</span></span>

## <span data-ttu-id="66859-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66859-122">RELATED LINKS</span></span>

[<span data-ttu-id="66859-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="66859-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="66859-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="66859-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


