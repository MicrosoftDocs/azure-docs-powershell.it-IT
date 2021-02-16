---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176607"
---
# <span data-ttu-id="dad06-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="dad06-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="dad06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad06-102">SYNOPSIS</span></span>
<span data-ttu-id="dad06-103">Recupera le proprietà delle metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dad06-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="dad06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dad06-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dad06-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dad06-105">DESCRIPTION</span></span>
<span data-ttu-id="dad06-106">Il cmdlet **Get-AzStorageServiceMetricsProperty ottiene** le proprietà delle metriche per il servizio di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dad06-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="dad06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dad06-107">EXAMPLES</span></span>

### <span data-ttu-id="dad06-108">Esempio 1: Ottenere le proprietà delle metriche per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="dad06-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="dad06-109">Questo comando recupera le proprietà delle metriche per l'archiviazione BLOB per il tipo di metriche Ora.</span><span class="sxs-lookup"><span data-stu-id="dad06-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="dad06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dad06-110">PARAMETERS</span></span>

### <span data-ttu-id="dad06-111">-Context</span><span class="sxs-lookup"><span data-stu-id="dad06-111">-Context</span></span>
<span data-ttu-id="dad06-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dad06-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dad06-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dad06-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad06-114">-DefaultProfile</span></span>
<span data-ttu-id="dad06-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dad06-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad06-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="dad06-116">-MetricsType</span></span>
<span data-ttu-id="dad06-117">Specifica un tipo di metriche.</span><span class="sxs-lookup"><span data-stu-id="dad06-117">Specifies a metrics type.</span></span>
<span data-ttu-id="dad06-118">Questo cmdlet ottiene le proprietà delle metriche del servizio di archiviazione di Azure per il tipo di metriche specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dad06-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="dad06-119">I valori accettabili per questo parametro sono: Ora e Minuto.</span><span class="sxs-lookup"><span data-stu-id="dad06-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad06-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="dad06-120">-ServiceType</span></span>
<span data-ttu-id="dad06-121">Specifica il tipo di servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dad06-121">Specifies the storage service type.</span></span>
<span data-ttu-id="dad06-122">Questo cmdlet ottiene le proprietà delle metriche per il tipo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dad06-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="dad06-123">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="dad06-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dad06-124">BLOB</span><span class="sxs-lookup"><span data-stu-id="dad06-124">Blob</span></span> 
- <span data-ttu-id="dad06-125">tavolo</span><span class="sxs-lookup"><span data-stu-id="dad06-125">Table</span></span>
- <span data-ttu-id="dad06-126">Coda</span><span class="sxs-lookup"><span data-stu-id="dad06-126">Queue</span></span>
- <span data-ttu-id="dad06-127">File Il valore di File non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="dad06-127">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad06-128">CommonParameters</span></span>
<span data-ttu-id="dad06-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad06-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad06-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad06-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="dad06-131">INPUTS</span></span>

### <span data-ttu-id="dad06-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dad06-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dad06-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dad06-133">OUTPUTS</span></span>

### <span data-ttu-id="dad06-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="dad06-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="dad06-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="dad06-135">NOTES</span></span>

## <span data-ttu-id="dad06-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dad06-136">RELATED LINKS</span></span>

[<span data-ttu-id="dad06-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dad06-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="dad06-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="dad06-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


