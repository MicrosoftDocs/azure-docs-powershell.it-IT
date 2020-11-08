---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023895"
---
# <span data-ttu-id="9d66c-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="9d66c-101">Test-AzureName</span></span>

## <span data-ttu-id="9d66c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d66c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d66c-103">Verifica se un nome del servizio cloud di Microsoft Azure, il nome del servizio di archiviazione o il nome dello spazio dei nomi Service Bus esiste oppure no.</span><span class="sxs-lookup"><span data-stu-id="9d66c-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="9d66c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d66c-104">SYNTAX</span></span>

### <span data-ttu-id="9d66c-105">Servizio</span><span class="sxs-lookup"><span data-stu-id="9d66c-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d66c-106">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="9d66c-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d66c-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9d66c-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d66c-108">Sito Web</span><span class="sxs-lookup"><span data-stu-id="9d66c-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d66c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d66c-109">DESCRIPTION</span></span>
<span data-ttu-id="9d66c-110">Se il nome esiste, il cmdlet restituisce $True.</span><span class="sxs-lookup"><span data-stu-id="9d66c-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="9d66c-111">Se il nome non esiste, restituisce $False.</span><span class="sxs-lookup"><span data-stu-id="9d66c-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="9d66c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d66c-112">EXAMPLES</span></span>

### <span data-ttu-id="9d66c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d66c-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="9d66c-114">Questo comando consente di verificare se "MyNameService1" è un nome di servizio cloud di Microsoft Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="9d66c-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="9d66c-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9d66c-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="9d66c-116">Questo comando consente di verificare se "mystorename1" è un nome del servizio di archiviazione di Microsoft Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="9d66c-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="9d66c-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9d66c-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="9d66c-118">Questo comando consente di verificare se "MyNamespace" è un nome dello spazio dei nomi di Microsoft Azure Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="9d66c-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="9d66c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d66c-119">PARAMETERS</span></span>

### <span data-ttu-id="9d66c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d66c-120">-Name</span></span>
<span data-ttu-id="9d66c-121">Specifica il nome dell'account del servizio o dello spazio di archiviazione da testare.</span><span class="sxs-lookup"><span data-stu-id="9d66c-121">Specifies the name of the service or storage account to test.</span></span>

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

### <span data-ttu-id="9d66c-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="9d66c-122">-Profile</span></span>
<span data-ttu-id="9d66c-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d66c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d66c-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9d66c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d66c-125">-Servizio</span><span class="sxs-lookup"><span data-stu-id="9d66c-125">-Service</span></span>
<span data-ttu-id="9d66c-126">Specifica di testare un account del servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="9d66c-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d66c-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9d66c-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="9d66c-128">Specifica di testare uno spazio dei nomi di Service Bus esistente.</span><span class="sxs-lookup"><span data-stu-id="9d66c-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d66c-129">-Spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9d66c-129">-Storage</span></span>
<span data-ttu-id="9d66c-130">Specifica di testare un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="9d66c-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d66c-131">-Sito Web</span><span class="sxs-lookup"><span data-stu-id="9d66c-131">-Website</span></span>
<span data-ttu-id="9d66c-132">Specifica di testare un sito Web esistente.</span><span class="sxs-lookup"><span data-stu-id="9d66c-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d66c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d66c-133">CommonParameters</span></span>
<span data-ttu-id="9d66c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d66c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d66c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d66c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d66c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d66c-136">INPUTS</span></span>

## <span data-ttu-id="9d66c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d66c-137">OUTPUTS</span></span>

## <span data-ttu-id="9d66c-138">Note</span><span class="sxs-lookup"><span data-stu-id="9d66c-138">NOTES</span></span>
* <span data-ttu-id="9d66c-139">node-dev, php-dev, python-dev</span><span class="sxs-lookup"><span data-stu-id="9d66c-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="9d66c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d66c-140">RELATED LINKS</span></span>

