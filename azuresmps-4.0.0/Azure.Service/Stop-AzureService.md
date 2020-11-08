---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023765"
---
# <span data-ttu-id="69b36-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="69b36-101">Stop-AzureService</span></span>

## <span data-ttu-id="69b36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69b36-102">SYNOPSIS</span></span>
<span data-ttu-id="69b36-103">Interrompe il servizio ospitato corrente.</span><span class="sxs-lookup"><span data-stu-id="69b36-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="69b36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69b36-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="69b36-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b36-105">DESCRIPTION</span></span>
<span data-ttu-id="69b36-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69b36-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="69b36-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="69b36-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="69b36-108">Il cmdlet **Stop-AzureService** interrompe il servizio ospitato corrente nello slot specificato in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="69b36-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="69b36-109">Se non viene specificato alcuno slot, il cmdlet arresta il servizio nello slot di produzione.</span><span class="sxs-lookup"><span data-stu-id="69b36-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="69b36-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69b36-110">EXAMPLES</span></span>

## <span data-ttu-id="69b36-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69b36-111">PARAMETERS</span></span>

### <span data-ttu-id="69b36-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69b36-112">-PassThru</span></span>
<span data-ttu-id="69b36-113">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="69b36-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69b36-114">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="69b36-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69b36-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="69b36-115">-Profile</span></span>
<span data-ttu-id="69b36-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69b36-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69b36-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="69b36-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69b36-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="69b36-118">-ServiceName</span></span>
<span data-ttu-id="69b36-119">Specifica il nome del servizio ospitato da interrompere.</span><span class="sxs-lookup"><span data-stu-id="69b36-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="69b36-120">Se non viene specificato alcun nome, il cmdlet arresta il servizio ospitato corrente.</span><span class="sxs-lookup"><span data-stu-id="69b36-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="69b36-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="69b36-121">-Slot</span></span>
<span data-ttu-id="69b36-122">Specifica lo slot in cui è ospitato il servizio, la gestione temporanea o la produzione.</span><span class="sxs-lookup"><span data-stu-id="69b36-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="69b36-123">Se non viene specificato alcuno slot, viene assunta la produzione.</span><span class="sxs-lookup"><span data-stu-id="69b36-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="69b36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b36-124">CommonParameters</span></span>
<span data-ttu-id="69b36-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b36-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b36-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b36-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69b36-127">INPUTS</span></span>

## <span data-ttu-id="69b36-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69b36-128">OUTPUTS</span></span>

## <span data-ttu-id="69b36-129">Note</span><span class="sxs-lookup"><span data-stu-id="69b36-129">NOTES</span></span>

## <span data-ttu-id="69b36-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69b36-130">RELATED LINKS</span></span>

[<span data-ttu-id="69b36-131">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="69b36-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="69b36-132">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="69b36-132">Start-AzureService</span></span>](./Start-AzureService.md)


