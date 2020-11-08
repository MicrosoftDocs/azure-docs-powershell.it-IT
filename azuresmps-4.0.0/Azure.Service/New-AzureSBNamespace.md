---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023946"
---
# <span data-ttu-id="db695-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="db695-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="db695-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db695-102">SYNOPSIS</span></span>
<span data-ttu-id="db695-103">Crea uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db695-103">Creates a namespace.</span></span>

## <span data-ttu-id="db695-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db695-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db695-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db695-105">DESCRIPTION</span></span>
<span data-ttu-id="db695-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db695-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="db695-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="db695-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="db695-108">Il cmdlet **New-AzureSBNamespace** crea uno spazio dei nomi del servizio da usare con Service Bus in Azure.</span><span class="sxs-lookup"><span data-stu-id="db695-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="db695-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db695-109">EXAMPLES</span></span>

### <span data-ttu-id="db695-110">Esempio 1: creare uno spazio dei nomi del servizio</span><span class="sxs-lookup"><span data-stu-id="db695-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="db695-111">Gli esempi creano uno spazio dei nomi del servizio da usare con Service Bus in Azure.</span><span class="sxs-lookup"><span data-stu-id="db695-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="db695-112">Entrambi gli esempi includono i valori dei parametri obbligatori, ma solo i primi includono i nomi dei parametri.</span><span class="sxs-lookup"><span data-stu-id="db695-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="db695-113">Il secondo esempio può essere usato perché entrambi i parametri sono posizionali e i relativi valori sono specificati nell'ordine richiesto.</span><span class="sxs-lookup"><span data-stu-id="db695-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="db695-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db695-114">PARAMETERS</span></span>

### <span data-ttu-id="db695-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="db695-115">-CreateACSNamespace</span></span>
<span data-ttu-id="db695-116">Specifica se creare uno spazio dei nomi ACS associato oltre allo spazio dei nomi del servizio.</span><span class="sxs-lookup"><span data-stu-id="db695-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db695-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="db695-117">-Location</span></span>
<span data-ttu-id="db695-118">Specifica un'area per il nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db695-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="db695-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="db695-119">-Name</span></span>
<span data-ttu-id="db695-120">Specifica un nome per il nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db695-120">Specifies a name for the new namespace.</span></span>

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

### <span data-ttu-id="db695-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="db695-121">-NamespaceType</span></span>
<span data-ttu-id="db695-122">Specifica se usare lo spazio dei nomi per gli hub di messaggistica o di notifica.</span><span class="sxs-lookup"><span data-stu-id="db695-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db695-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="db695-123">-Profile</span></span>
<span data-ttu-id="db695-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db695-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db695-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="db695-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db695-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db695-126">CommonParameters</span></span>
<span data-ttu-id="db695-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db695-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db695-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db695-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db695-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db695-129">INPUTS</span></span>

## <span data-ttu-id="db695-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db695-130">OUTPUTS</span></span>

## <span data-ttu-id="db695-131">Note</span><span class="sxs-lookup"><span data-stu-id="db695-131">NOTES</span></span>

## <span data-ttu-id="db695-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db695-132">RELATED LINKS</span></span>

[<span data-ttu-id="db695-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="db695-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


