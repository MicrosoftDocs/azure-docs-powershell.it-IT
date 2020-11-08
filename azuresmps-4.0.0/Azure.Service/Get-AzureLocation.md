---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029798"
---
# <span data-ttu-id="393d8-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="393d8-101">Get-AzureLocation</span></span>

## <span data-ttu-id="393d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="393d8-102">SYNOPSIS</span></span>
<span data-ttu-id="393d8-103">Ottiene le posizioni del centro dati disponibili per l'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="393d8-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="393d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="393d8-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="393d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="393d8-105">DESCRIPTION</span></span>
<span data-ttu-id="393d8-106">Il cmdlet **Get-AzureLocation** ottiene un elenco dei Data Center di Azure disponibili e delle relative proprietà per l'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="393d8-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="393d8-107">Prima di eseguire questo cmdlet, è necessario impostare l'abbonamento corrente usando i cmdlet Select-AzureSubscription e Set-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="393d8-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="393d8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="393d8-108">EXAMPLES</span></span>

### <span data-ttu-id="393d8-109">Esempio 1: ottenere posizioni</span><span class="sxs-lookup"><span data-stu-id="393d8-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="393d8-110">Questo comando consente di ottenere un elenco di data center disponibili e le relative proprietà per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="393d8-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="393d8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="393d8-111">PARAMETERS</span></span>

### <span data-ttu-id="393d8-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="393d8-112">-InformationAction</span></span>
<span data-ttu-id="393d8-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="393d8-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="393d8-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="393d8-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="393d8-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="393d8-115">Continue</span></span>
- <span data-ttu-id="393d8-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="393d8-116">Ignore</span></span>
- <span data-ttu-id="393d8-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="393d8-117">Inquire</span></span>
- <span data-ttu-id="393d8-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="393d8-118">SilentlyContinue</span></span>
- <span data-ttu-id="393d8-119">Stop</span><span class="sxs-lookup"><span data-stu-id="393d8-119">Stop</span></span>
- <span data-ttu-id="393d8-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="393d8-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393d8-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="393d8-121">-InformationVariable</span></span>
<span data-ttu-id="393d8-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="393d8-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393d8-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="393d8-123">-Profile</span></span>
<span data-ttu-id="393d8-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="393d8-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="393d8-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="393d8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="393d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393d8-126">CommonParameters</span></span>
<span data-ttu-id="393d8-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393d8-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393d8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393d8-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="393d8-129">INPUTS</span></span>

## <span data-ttu-id="393d8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="393d8-130">OUTPUTS</span></span>

## <span data-ttu-id="393d8-131">Note</span><span class="sxs-lookup"><span data-stu-id="393d8-131">NOTES</span></span>

## <span data-ttu-id="393d8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="393d8-132">RELATED LINKS</span></span>

