---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029511"
---
# <span data-ttu-id="42993-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="42993-101">Set-AzureService</span></span>

## <span data-ttu-id="42993-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42993-102">SYNOPSIS</span></span>
<span data-ttu-id="42993-103">Imposta o aggiorna l'etichetta e la descrizione del servizio Microsoft Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="42993-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="42993-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42993-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="42993-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42993-105">DESCRIPTION</span></span>
<span data-ttu-id="42993-106">Il cmdlet **set-AzureService** assegna un'etichetta e una descrizione a un servizio nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="42993-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="42993-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42993-107">EXAMPLES</span></span>

### <span data-ttu-id="42993-108">Esempio 1: aggiornare l'etichetta e la descrizione di un servizio</span><span class="sxs-lookup"><span data-stu-id="42993-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="42993-109">Questo comando imposta l'etichetta su "MyTestSvc1" e la descrizione su "il mio servizio per testare le nuove configurazioni" per il servizio MyTestSvc1.</span><span class="sxs-lookup"><span data-stu-id="42993-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="42993-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42993-110">PARAMETERS</span></span>

### <span data-ttu-id="42993-111">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="42993-111">-Description</span></span>
<span data-ttu-id="42993-112">Specifica una descrizione per il servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="42993-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="42993-113">La descrizione può contenere fino a 1024 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="42993-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42993-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="42993-114">-InformationAction</span></span>
<span data-ttu-id="42993-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="42993-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="42993-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="42993-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42993-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="42993-117">Continue</span></span>
- <span data-ttu-id="42993-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="42993-118">Ignore</span></span>
- <span data-ttu-id="42993-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="42993-119">Inquire</span></span>
- <span data-ttu-id="42993-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="42993-120">SilentlyContinue</span></span>
- <span data-ttu-id="42993-121">Stop</span><span class="sxs-lookup"><span data-stu-id="42993-121">Stop</span></span>
- <span data-ttu-id="42993-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="42993-122">Suspend</span></span>

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

### <span data-ttu-id="42993-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="42993-123">-InformationVariable</span></span>
<span data-ttu-id="42993-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="42993-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="42993-125">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="42993-125">-Label</span></span>
<span data-ttu-id="42993-126">Specifica un'etichetta per il servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="42993-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="42993-127">L'etichetta può contenere fino a 100 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="42993-127">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42993-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="42993-128">-Profile</span></span>
<span data-ttu-id="42993-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42993-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42993-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="42993-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42993-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="42993-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="42993-132">Specifica il nome di dominio completo per il DNS inverso.</span><span class="sxs-lookup"><span data-stu-id="42993-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42993-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="42993-133">-ServiceName</span></span>
<span data-ttu-id="42993-134">Specifica il nome del servizio Azure da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="42993-134">Specifies the name of the Azure service to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42993-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42993-135">CommonParameters</span></span>
<span data-ttu-id="42993-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42993-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42993-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42993-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42993-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42993-138">INPUTS</span></span>

## <span data-ttu-id="42993-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42993-139">OUTPUTS</span></span>

### <span data-ttu-id="42993-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="42993-140">ManagementOperationContext</span></span>

## <span data-ttu-id="42993-141">Note</span><span class="sxs-lookup"><span data-stu-id="42993-141">NOTES</span></span>

## <span data-ttu-id="42993-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42993-142">RELATED LINKS</span></span>

[<span data-ttu-id="42993-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="42993-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="42993-144">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="42993-144">New-AzureService</span></span>](./New-AzureService.md)


