---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 0c1d847045cc4fb8be39674c13c38114ee9d3a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675653"
---
# <span data-ttu-id="a4b3c-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a4b3c-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="a4b3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b3c-103">Aggiunge un'applicazione all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="a4b3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4b3c-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b3c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b3c-106">Il cmdlet **New-AzBatchApplication** aggiunge un'applicazione all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="a4b3c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4b3c-107">EXAMPLES</span></span>

### <span data-ttu-id="a4b3c-108">Esempio 1: aggiungere un'applicazione vuota a un account batch</span><span class="sxs-lookup"><span data-stu-id="a4b3c-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="a4b3c-109">Questo comando crea l'applicazione Litware nell'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="a4b3c-110">L'applicazione inizialmente non contiene pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="a4b3c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4b3c-111">PARAMETERS</span></span>

### <span data-ttu-id="a4b3c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4b3c-112">-AccountName</span></span>
<span data-ttu-id="a4b3c-113">Specifica il nome dell'account batch a cui questo cmdlet aggiunge un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="a4b3c-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="a4b3c-114">-AllowUpdates</span></span>
<span data-ttu-id="a4b3c-115">Specifica se i pacchetti all'interno dell'applicazione possono essere sovrascritti usando la stessa stringa di versione.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b3c-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a4b3c-116">-ApplicationId</span></span>
<span data-ttu-id="a4b3c-117">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b3c-118">-DefaultProfile</span></span>
<span data-ttu-id="a4b3c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4b3c-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a4b3c-120">-DisplayName</span></span>
<span data-ttu-id="a4b3c-121">Specifica il nome visualizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b3c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b3c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4b3c-123">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a4b3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b3c-124">CommonParameters</span></span>
<span data-ttu-id="a4b3c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b3c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b3c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b3c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4b3c-127">INPUTS</span></span>

### <span data-ttu-id="a4b3c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b3c-128">System.String</span></span>

### <span data-ttu-id="a4b3c-129">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a4b3c-129">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a4b3c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4b3c-130">OUTPUTS</span></span>

### <span data-ttu-id="a4b3c-131">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a4b3c-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="a4b3c-132">Note</span><span class="sxs-lookup"><span data-stu-id="a4b3c-132">NOTES</span></span>

## <span data-ttu-id="a4b3c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4b3c-133">RELATED LINKS</span></span>

[<span data-ttu-id="a4b3c-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a4b3c-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="a4b3c-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a4b3c-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="a4b3c-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a4b3c-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="a4b3c-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a4b3c-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="a4b3c-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a4b3c-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="a4b3c-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a4b3c-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


