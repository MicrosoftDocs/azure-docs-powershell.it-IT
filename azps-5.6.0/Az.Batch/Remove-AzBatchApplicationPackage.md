---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: 7c51776683d4a8ecb777fd56d8b83ca4ae672206
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969693"
---
# <span data-ttu-id="7457b-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7457b-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="7457b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7457b-102">SYNOPSIS</span></span>
<span data-ttu-id="7457b-103">Elimina un record del pacchetto dell'applicazione e il file binario.</span><span class="sxs-lookup"><span data-stu-id="7457b-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="7457b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7457b-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7457b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7457b-105">DESCRIPTION</span></span>
<span data-ttu-id="7457b-106">Il cmdlet **Remove-AzBatchApplicationPackage** elimina un record del pacchetto dell'applicazione e il file binario da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7457b-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="7457b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7457b-107">EXAMPLES</span></span>

### <span data-ttu-id="7457b-108">Esempio 1: Eliminare un pacchetto dell'applicazione da un account Batch</span><span class="sxs-lookup"><span data-stu-id="7457b-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="7457b-109">Questo comando elimina la versione 1.0 dell'applicazione Litware dall'account ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="7457b-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="7457b-110">Il comando elimina sia il record del pacchetto che il BLOB che contiene il file binario del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7457b-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="7457b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7457b-111">PARAMETERS</span></span>

### <span data-ttu-id="7457b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7457b-112">-AccountName</span></span>
<span data-ttu-id="7457b-113">Specifica il nome dell'account batch da cui questo cmdlet elimina un pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7457b-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="7457b-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="7457b-114">-ApplicationName</span></span>
<span data-ttu-id="7457b-115">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7457b-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="7457b-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="7457b-116">-ApplicationVersion</span></span>
<span data-ttu-id="7457b-117">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7457b-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7457b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7457b-118">-DefaultProfile</span></span>
<span data-ttu-id="7457b-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7457b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7457b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7457b-120">-ResourceGroupName</span></span>
<span data-ttu-id="7457b-121">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="7457b-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="7457b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7457b-122">CommonParameters</span></span>
<span data-ttu-id="7457b-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7457b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7457b-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7457b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7457b-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="7457b-125">INPUTS</span></span>

### <span data-ttu-id="7457b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7457b-126">System.String</span></span>

## <span data-ttu-id="7457b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7457b-127">OUTPUTS</span></span>

### <span data-ttu-id="7457b-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="7457b-128">System.Void</span></span>

## <span data-ttu-id="7457b-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="7457b-129">NOTES</span></span>

## <span data-ttu-id="7457b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7457b-130">RELATED LINKS</span></span>

[<span data-ttu-id="7457b-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7457b-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="7457b-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7457b-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="7457b-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7457b-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="7457b-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7457b-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="7457b-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7457b-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="7457b-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7457b-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


