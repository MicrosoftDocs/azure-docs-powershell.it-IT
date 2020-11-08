---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029792"
---
# <span data-ttu-id="35cf7-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="35cf7-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="35cf7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="35cf7-103">Recupera un riepilogo di utilizzo per una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="35cf7-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="35cf7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35cf7-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="35cf7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="35cf7-106">Il cmdlet **Get-AzureRemoteAppCollectionUsageSummary** recupera un riepilogo di utilizzo per una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="35cf7-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="35cf7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35cf7-107">EXAMPLES</span></span>

### <span data-ttu-id="35cf7-108">Esempio 1: ottenere un riepilogo dell'utilizzo</span><span class="sxs-lookup"><span data-stu-id="35cf7-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="35cf7-109">Questo comando ottiene un riepilogo dell'utilizzo per il mese di dicembre dell'anno 2014, per una raccolta denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="35cf7-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="35cf7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35cf7-110">PARAMETERS</span></span>

### <span data-ttu-id="35cf7-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="35cf7-111">-CollectionName</span></span>
<span data-ttu-id="35cf7-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="35cf7-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35cf7-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="35cf7-113">-Profile</span></span>
<span data-ttu-id="35cf7-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35cf7-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35cf7-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="35cf7-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="35cf7-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="35cf7-116">-UsageMonth</span></span>
<span data-ttu-id="35cf7-117">Specifica un numero a due cifre per il mese per cui ottenere un riepilogo dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="35cf7-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="35cf7-118">Se questo parametro non viene specificato, questo cmdlet fornisce l'utilizzo per il mese corrente.</span><span class="sxs-lookup"><span data-stu-id="35cf7-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35cf7-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="35cf7-119">-UsageYear</span></span>
<span data-ttu-id="35cf7-120">Specifica l'anno a quattro cifre per cui ottenere un riepilogo dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="35cf7-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="35cf7-121">Se questo parametro non viene specificato, verrà usato questo cmdlet per l'anno corrente.</span><span class="sxs-lookup"><span data-stu-id="35cf7-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35cf7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cf7-122">CommonParameters</span></span>
<span data-ttu-id="35cf7-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35cf7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cf7-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35cf7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cf7-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35cf7-125">INPUTS</span></span>

## <span data-ttu-id="35cf7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35cf7-126">OUTPUTS</span></span>

## <span data-ttu-id="35cf7-127">Note</span><span class="sxs-lookup"><span data-stu-id="35cf7-127">NOTES</span></span>

## <span data-ttu-id="35cf7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35cf7-128">RELATED LINKS</span></span>

[<span data-ttu-id="35cf7-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="35cf7-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="35cf7-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="35cf7-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


