---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030033"
---
# <span data-ttu-id="4d547-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="4d547-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="4d547-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d547-102">SYNOPSIS</span></span>
<span data-ttu-id="4d547-103">Ottiene le macchine virtuali in una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d547-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="4d547-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d547-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4d547-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d547-105">DESCRIPTION</span></span>
<span data-ttu-id="4d547-106">Il cmdlet **Get-AzureRemoteAppVM** ottiene le macchine virtuali create in una raccolta RemoteApp di Azure per l'hosting della sessione.</span><span class="sxs-lookup"><span data-stu-id="4d547-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="4d547-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d547-107">EXAMPLES</span></span>

### <span data-ttu-id="4d547-108">Esempio 1: visualizzare le macchine virtuali in una raccolta</span><span class="sxs-lookup"><span data-stu-id="4d547-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="4d547-109">Questo comando Visualizza le macchine virtuali usate per l'hosting della sessione in una raccolta RemoteApp di Azure denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="4d547-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="4d547-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d547-110">PARAMETERS</span></span>

### <span data-ttu-id="4d547-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="4d547-111">-CollectionName</span></span>
<span data-ttu-id="4d547-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d547-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d547-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="4d547-113">-Profile</span></span>
<span data-ttu-id="4d547-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d547-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4d547-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="4d547-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4d547-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d547-116">CommonParameters</span></span>
<span data-ttu-id="4d547-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d547-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d547-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d547-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d547-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d547-119">INPUTS</span></span>

## <span data-ttu-id="4d547-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d547-120">OUTPUTS</span></span>

## <span data-ttu-id="4d547-121">Note</span><span class="sxs-lookup"><span data-stu-id="4d547-121">NOTES</span></span>

## <span data-ttu-id="4d547-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d547-122">RELATED LINKS</span></span>

[<span data-ttu-id="4d547-123">Riavviare-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="4d547-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


