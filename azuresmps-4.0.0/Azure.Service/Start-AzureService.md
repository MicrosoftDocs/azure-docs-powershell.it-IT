---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029492"
---
# <span data-ttu-id="9dde5-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="9dde5-101">Start-AzureService</span></span>

## <span data-ttu-id="9dde5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dde5-102">SYNOPSIS</span></span>
<span data-ttu-id="9dde5-103">Avvia il servizio ospitato specificato in Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="9dde5-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="9dde5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dde5-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9dde5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dde5-105">DESCRIPTION</span></span>
<span data-ttu-id="9dde5-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9dde5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9dde5-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9dde5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9dde5-108">Il cmdlet **Start-AzureService** avvia il servizio ospitato specificato in Windows Azure, se il servizio si trova nello stato Stopped.</span><span class="sxs-lookup"><span data-stu-id="9dde5-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="9dde5-109">Tieni presente che il cmdlet **Publish-AzureServiceProject** tenta automaticamente di avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="9dde5-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="9dde5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dde5-110">EXAMPLES</span></span>

## <span data-ttu-id="9dde5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dde5-111">PARAMETERS</span></span>

### <span data-ttu-id="9dde5-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dde5-112">-PassThru</span></span>
<span data-ttu-id="9dde5-113">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9dde5-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9dde5-114">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9dde5-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9dde5-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="9dde5-115">-Profile</span></span>
<span data-ttu-id="9dde5-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dde5-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9dde5-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9dde5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9dde5-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9dde5-118">-ServiceName</span></span>
<span data-ttu-id="9dde5-119">Specifica il nome del servizio ospitato da avviare.</span><span class="sxs-lookup"><span data-stu-id="9dde5-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="9dde5-120">Se non viene specificato alcun nome, il cmdlet avvia il servizio ospitato corrente.</span><span class="sxs-lookup"><span data-stu-id="9dde5-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="9dde5-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="9dde5-121">-Slot</span></span>
<span data-ttu-id="9dde5-122">Specifica lo slot di distribuzione in cui avviare il servizio, ovvero la gestione temporanea o la produzione.</span><span class="sxs-lookup"><span data-stu-id="9dde5-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="9dde5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dde5-123">CommonParameters</span></span>
<span data-ttu-id="9dde5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dde5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dde5-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dde5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dde5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dde5-126">INPUTS</span></span>

## <span data-ttu-id="9dde5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dde5-127">OUTPUTS</span></span>

## <span data-ttu-id="9dde5-128">Note</span><span class="sxs-lookup"><span data-stu-id="9dde5-128">NOTES</span></span>

## <span data-ttu-id="9dde5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dde5-129">RELATED LINKS</span></span>

[<span data-ttu-id="9dde5-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="9dde5-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="9dde5-131">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="9dde5-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="9dde5-132">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="9dde5-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


