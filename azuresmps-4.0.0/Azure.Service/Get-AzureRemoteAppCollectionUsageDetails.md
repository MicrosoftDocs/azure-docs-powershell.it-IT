---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023590"
---
# <span data-ttu-id="7877a-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="7877a-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="7877a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7877a-102">SYNOPSIS</span></span>
<span data-ttu-id="7877a-103">Recupera i dettagli sull'utilizzo di una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="7877a-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7877a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7877a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7877a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7877a-105">DESCRIPTION</span></span>
<span data-ttu-id="7877a-106">Il cmdlet **Get-AzureRemoteAppCollectionUsageDetails** recupera i dettagli sull'utilizzo di una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="7877a-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7877a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7877a-107">EXAMPLES</span></span>

### <span data-ttu-id="7877a-108">Esempio 1: ottenere i dettagli sull'utilizzo per una raccolta</span><span class="sxs-lookup"><span data-stu-id="7877a-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="7877a-109">Questo comando ottiene i dettagli sull'utilizzo per il mese di dicembre dell'anno 2014, per una raccolta RemoteApp di Azure denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="7877a-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="7877a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7877a-110">PARAMETERS</span></span>

### <span data-ttu-id="7877a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7877a-111">-AsJob</span></span>
<span data-ttu-id="7877a-112">Indica che il cmdlet viene eseguito in background come processo di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7877a-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

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

### <span data-ttu-id="7877a-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="7877a-113">-CollectionName</span></span>
<span data-ttu-id="7877a-114">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="7877a-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="7877a-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="7877a-115">-Profile</span></span>
<span data-ttu-id="7877a-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7877a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7877a-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7877a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7877a-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="7877a-118">-UsageMonth</span></span>
<span data-ttu-id="7877a-119">Specifica un numero a due cifre per il mese per cui ottenere i dettagli sull'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="7877a-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="7877a-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="7877a-120">-UsageYear</span></span>
<span data-ttu-id="7877a-121">Specifica l'anno a quattro cifre per cui ottenere i dettagli sull'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="7877a-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="7877a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7877a-122">CommonParameters</span></span>
<span data-ttu-id="7877a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7877a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7877a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7877a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7877a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7877a-125">INPUTS</span></span>

## <span data-ttu-id="7877a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7877a-126">OUTPUTS</span></span>

## <span data-ttu-id="7877a-127">Note</span><span class="sxs-lookup"><span data-stu-id="7877a-127">NOTES</span></span>

## <span data-ttu-id="7877a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7877a-128">RELATED LINKS</span></span>

[<span data-ttu-id="7877a-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="7877a-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="7877a-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="7877a-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


