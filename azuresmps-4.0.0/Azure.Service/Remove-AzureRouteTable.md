---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029594"
---
# <span data-ttu-id="86554-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="86554-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="86554-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86554-102">SYNOPSIS</span></span>
<span data-ttu-id="86554-103">Rimuove una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="86554-103">Removes a route table.</span></span>

## <span data-ttu-id="86554-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86554-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86554-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86554-105">DESCRIPTION</span></span>
<span data-ttu-id="86554-106">Il cmdlet **Remove-AzureRouteTable** rimuove una tabella di route dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="86554-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="86554-107">Se una tabella di route è associata a una subnet, non è possibile rimuovere la tabella.</span><span class="sxs-lookup"><span data-stu-id="86554-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="86554-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86554-108">EXAMPLES</span></span>

### <span data-ttu-id="86554-109">Esempio 1: rimuovere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="86554-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="86554-110">Questo comando rimuove la tabella di route denominata PublicRouteTable.</span><span class="sxs-lookup"><span data-stu-id="86554-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="86554-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86554-111">PARAMETERS</span></span>

### <span data-ttu-id="86554-112">-Force</span><span class="sxs-lookup"><span data-stu-id="86554-112">-Force</span></span>
<span data-ttu-id="86554-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="86554-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="86554-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="86554-114">-Name</span></span>
<span data-ttu-id="86554-115">Specifica il nome della tabella di route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86554-115">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86554-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86554-116">-PassThru</span></span>
<span data-ttu-id="86554-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="86554-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86554-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="86554-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86554-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="86554-119">-Profile</span></span>
<span data-ttu-id="86554-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86554-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86554-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="86554-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86554-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86554-122">CommonParameters</span></span>
<span data-ttu-id="86554-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86554-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86554-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86554-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86554-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86554-125">INPUTS</span></span>

## <span data-ttu-id="86554-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86554-126">OUTPUTS</span></span>

## <span data-ttu-id="86554-127">Note</span><span class="sxs-lookup"><span data-stu-id="86554-127">NOTES</span></span>

## <span data-ttu-id="86554-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86554-128">RELATED LINKS</span></span>

[<span data-ttu-id="86554-129">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="86554-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="86554-130">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="86554-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
