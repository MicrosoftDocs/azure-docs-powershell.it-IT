---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029974"
---
# <span data-ttu-id="f690e-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="f690e-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="f690e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f690e-102">SYNOPSIS</span></span>
<span data-ttu-id="f690e-103">Ottiene i piani di hosting Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f690e-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="f690e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f690e-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f690e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f690e-105">DESCRIPTION</span></span>
<span data-ttu-id="f690e-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f690e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f690e-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f690e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f690e-108">Il cmdlet **Get-AzureWebHostingPlan** ottiene i piani di hosting Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f690e-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="f690e-109">Per impostazione predefinita, **Get-AzureWebHostingPlan** ottiene tutti i piani di hosting di Azure nell'abbonamento corrente e restituisce un oggetto che fornisce informazioni di base sui piani.</span><span class="sxs-lookup"><span data-stu-id="f690e-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="f690e-110">Quando usi i parametri *webspace* e *Name* , **Get-AzureWebHostingPlan** restituisce un oggetto piano di hosting specifico.</span><span class="sxs-lookup"><span data-stu-id="f690e-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="f690e-111">Per trovare l'abbonamento corrente, usa il parametro *Current* del cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="f690e-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="f690e-112">Per cambiare l'abbonamento corrente, usare il cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="f690e-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="f690e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f690e-113">EXAMPLES</span></span>

### <span data-ttu-id="f690e-114">Esempio 1: ottenere tutti i piani di hosting Web in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="f690e-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="f690e-115">Questo comando ottiene tutti i piani di hosting Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f690e-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="f690e-116">Esempio 2: ottenere un piano di hosting Web specifico in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="f690e-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="f690e-117">Questo comando ottiene il piano di hosting Web denominato Default0 nella barra multispazio denominata westeuropewebspace nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f690e-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="f690e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f690e-118">PARAMETERS</span></span>

### <span data-ttu-id="f690e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f690e-119">-Name</span></span>
<span data-ttu-id="f690e-120">Specifica il nome di un piano nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f690e-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="f690e-121">Per impostazione predefinita, questo cmdlet ottiene tutti i piani della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f690e-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="f690e-122">Questo parametro non supporta i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="f690e-122">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f690e-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="f690e-123">-Profile</span></span>
<span data-ttu-id="f690e-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f690e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f690e-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f690e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f690e-126">-Webspacename</span><span class="sxs-lookup"><span data-stu-id="f690e-126">-WebSpaceName</span></span>
<span data-ttu-id="f690e-127">Specifica il nome di uno spazio Web nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f690e-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="f690e-128">Per impostazione predefinita, questo cmdlet recupera tutti i siti Web nel webspace specificato.</span><span class="sxs-lookup"><span data-stu-id="f690e-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="f690e-129">Questo parametro non supporta i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="f690e-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f690e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f690e-130">CommonParameters</span></span>
<span data-ttu-id="f690e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f690e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f690e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f690e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f690e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f690e-133">INPUTS</span></span>

###  
<span data-ttu-id="f690e-134">Puoi passare l'input al cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="f690e-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f690e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f690e-135">OUTPUTS</span></span>

### <span data-ttu-id="f690e-136">Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="f690e-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="f690e-137">Per impostazione predefinita, **Get-AzureWebHostingPlan** restituisce una matrice di oggetti **WebHostingPlan** .</span><span class="sxs-lookup"><span data-stu-id="f690e-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="f690e-138">Note</span><span class="sxs-lookup"><span data-stu-id="f690e-138">NOTES</span></span>

## <span data-ttu-id="f690e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f690e-139">RELATED LINKS</span></span>

