---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330967"
---
# <span data-ttu-id="67d91-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67d91-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="67d91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67d91-102">SYNOPSIS</span></span>
<span data-ttu-id="67d91-103">Ottiene le informazioni su un pacchetto di applicazione in un account batch.</span><span class="sxs-lookup"><span data-stu-id="67d91-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="67d91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67d91-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67d91-105">DESCRIPTION</span></span>
<span data-ttu-id="67d91-106">Il cmdlet **Get-AzBatchApplicationPackage** ottiene le informazioni su un pacchetto dell'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="67d91-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="67d91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67d91-107">EXAMPLES</span></span>

### <span data-ttu-id="67d91-108">Esempio 1: ottenere informazioni dettagliate su un pacchetto di applicazione in un account batch</span><span class="sxs-lookup"><span data-stu-id="67d91-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="67d91-109">Questo comando consente di ottenere i dettagli della versione 1,0 del pacchetto Litware.</span><span class="sxs-lookup"><span data-stu-id="67d91-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="67d91-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67d91-110">PARAMETERS</span></span>

### <span data-ttu-id="67d91-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67d91-111">-AccountName</span></span>
<span data-ttu-id="67d91-112">Specifica il nome dell'account batch da cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="67d91-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d91-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="67d91-113">-ApplicationName</span></span>
<span data-ttu-id="67d91-114">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67d91-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d91-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="67d91-115">-ApplicationVersion</span></span>
<span data-ttu-id="67d91-116">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="67d91-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d91-117">-DefaultProfile</span></span>
<span data-ttu-id="67d91-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67d91-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d91-119">-ResourceGroupName</span></span>
<span data-ttu-id="67d91-120">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="67d91-120">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d91-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d91-121">CommonParameters</span></span>
<span data-ttu-id="67d91-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d91-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d91-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67d91-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d91-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67d91-124">INPUTS</span></span>

### <span data-ttu-id="67d91-125">System. String</span><span class="sxs-lookup"><span data-stu-id="67d91-125">System.String</span></span>

## <span data-ttu-id="67d91-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67d91-126">OUTPUTS</span></span>

### <span data-ttu-id="67d91-127">Microsoft.Azure.Commands.Batch. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67d91-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="67d91-128">Note</span><span class="sxs-lookup"><span data-stu-id="67d91-128">NOTES</span></span>

## <span data-ttu-id="67d91-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67d91-129">RELATED LINKS</span></span>

[<span data-ttu-id="67d91-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67d91-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="67d91-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67d91-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="67d91-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67d91-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="67d91-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67d91-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="67d91-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="67d91-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="67d91-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="67d91-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


