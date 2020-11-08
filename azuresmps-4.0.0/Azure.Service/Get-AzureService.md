---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029771"
---
# <span data-ttu-id="c6d84-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="c6d84-101">Get-AzureService</span></span>

## <span data-ttu-id="c6d84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6d84-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d84-103">Restituisce un oggetto con le informazioni sui servizi cloud per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c6d84-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="c6d84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6d84-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c6d84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6d84-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d84-106">Il cmdlet **Get-AzureService** restituisce un oggetto List con tutti i servizi cloud di Azure associati alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c6d84-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="c6d84-107">Se specifichi il parametro *ServiceName* , **Get-AzureService** restituirà informazioni solo sul servizio corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c6d84-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="c6d84-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6d84-108">EXAMPLES</span></span>

### <span data-ttu-id="c6d84-109">Esempio 1: ottenere informazioni su tutti i servizi</span><span class="sxs-lookup"><span data-stu-id="c6d84-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="c6d84-110">Questo comando restituisce un oggetto che contiene informazioni su tutti i servizi di Azure associati alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c6d84-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="c6d84-111">Esempio 2: ottenere informazioni su un servizio specificato</span><span class="sxs-lookup"><span data-stu-id="c6d84-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="c6d84-112">Questo comando restituisce informazioni sul servizio $MySvc.</span><span class="sxs-lookup"><span data-stu-id="c6d84-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="c6d84-113">Esempio 3: visualizzare i metodi e le proprietà disponibili</span><span class="sxs-lookup"><span data-stu-id="c6d84-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="c6d84-114">Questo comando Visualizza le proprietà e i metodi disponibili nel cmdlet **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="c6d84-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="c6d84-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6d84-115">PARAMETERS</span></span>

### <span data-ttu-id="c6d84-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c6d84-116">-InformationAction</span></span>
<span data-ttu-id="c6d84-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c6d84-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6d84-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6d84-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6d84-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="c6d84-119">Continue</span></span>
- <span data-ttu-id="c6d84-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="c6d84-120">Ignore</span></span>
- <span data-ttu-id="c6d84-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c6d84-121">Inquire</span></span>
- <span data-ttu-id="c6d84-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6d84-122">SilentlyContinue</span></span>
- <span data-ttu-id="c6d84-123">Stop</span><span class="sxs-lookup"><span data-stu-id="c6d84-123">Stop</span></span>
- <span data-ttu-id="c6d84-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c6d84-124">Suspend</span></span>

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

### <span data-ttu-id="c6d84-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6d84-125">-InformationVariable</span></span>
<span data-ttu-id="c6d84-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c6d84-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c6d84-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="c6d84-127">-Profile</span></span>
<span data-ttu-id="c6d84-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6d84-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6d84-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c6d84-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6d84-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c6d84-130">-ServiceName</span></span>
<span data-ttu-id="c6d84-131">Specifica il nome di un servizio in cui restituire le informazioni.</span><span class="sxs-lookup"><span data-stu-id="c6d84-131">Specifies the name of a service on which to return information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d84-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d84-132">CommonParameters</span></span>
<span data-ttu-id="c6d84-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6d84-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d84-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d84-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d84-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6d84-135">INPUTS</span></span>

## <span data-ttu-id="c6d84-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6d84-136">OUTPUTS</span></span>

### <span data-ttu-id="c6d84-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="c6d84-137">HostedServiceContext</span></span>

## <span data-ttu-id="c6d84-138">Note</span><span class="sxs-lookup"><span data-stu-id="c6d84-138">NOTES</span></span>

## <span data-ttu-id="c6d84-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6d84-139">RELATED LINKS</span></span>

[<span data-ttu-id="c6d84-140">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="c6d84-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="c6d84-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="c6d84-141">Set-AzureService</span></span>](./Set-AzureService.md)


