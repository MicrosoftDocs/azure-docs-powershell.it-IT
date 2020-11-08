---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023947"
---
# <span data-ttu-id="79a43-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="79a43-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="79a43-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79a43-102">SYNOPSIS</span></span>
<span data-ttu-id="79a43-103">Crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79a43-103">Creates a route table.</span></span>

## <span data-ttu-id="79a43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79a43-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="79a43-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79a43-105">DESCRIPTION</span></span>
<span data-ttu-id="79a43-106">Il cmdlet **New-AzureRouteTable** crea una tabella di route in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="79a43-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="79a43-107">È possibile aggiungere route definite dall'utente alla tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79a43-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="79a43-108">È possibile associare la tabella di route a una subnet in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="79a43-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="79a43-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79a43-109">EXAMPLES</span></span>

## <span data-ttu-id="79a43-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79a43-110">PARAMETERS</span></span>

### <span data-ttu-id="79a43-111">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="79a43-111">-Label</span></span>
<span data-ttu-id="79a43-112">Specifica una descrizione per la nuova tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79a43-112">Specifies a description for the new route table.</span></span>

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

### <span data-ttu-id="79a43-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="79a43-113">-Location</span></span>
<span data-ttu-id="79a43-114">Specifica la posizione in cui questo cmdlet crea la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79a43-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="79a43-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="79a43-115">-Name</span></span>
<span data-ttu-id="79a43-116">Specifica un nome per la tabella di route creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a43-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="79a43-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="79a43-117">-Profile</span></span>
<span data-ttu-id="79a43-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a43-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="79a43-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="79a43-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79a43-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a43-120">CommonParameters</span></span>
<span data-ttu-id="79a43-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a43-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a43-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a43-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a43-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79a43-123">INPUTS</span></span>

## <span data-ttu-id="79a43-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79a43-124">OUTPUTS</span></span>

## <span data-ttu-id="79a43-125">Note</span><span class="sxs-lookup"><span data-stu-id="79a43-125">NOTES</span></span>

## <span data-ttu-id="79a43-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79a43-126">RELATED LINKS</span></span>

[<span data-ttu-id="79a43-127">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="79a43-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="79a43-128">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="79a43-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


