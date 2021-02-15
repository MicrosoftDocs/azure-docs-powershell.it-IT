---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f88994649281d442f37a2bafa2cf2b4f74e6b86e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197015"
---
# <span data-ttu-id="0fbd7-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0fbd7-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="0fbd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fbd7-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbd7-103">Elimina un record del pacchetto dell'applicazione e il file binario.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="0fbd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fbd7-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationName] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fbd7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0fbd7-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbd7-106">Il cmdlet **Remove-AzBatchApplicationPackage** elimina un record del pacchetto dell'applicazione e il file binario da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="0fbd7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fbd7-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbd7-108">Esempio 1: Eliminare un pacchetto dell'applicazione da un account Batch</span><span class="sxs-lookup"><span data-stu-id="0fbd7-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="0fbd7-109">Questo comando elimina la versione 1.0 dell'applicazione Litware dall'account ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="0fbd7-110">Il comando elimina sia il record del pacchetto che il BLOB che contiene il file binario del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="0fbd7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fbd7-111">PARAMETERS</span></span>

### <span data-ttu-id="0fbd7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0fbd7-112">-AccountName</span></span>
<span data-ttu-id="0fbd7-113">Specifica il nome dell'account batch da cui questo cmdlet elimina un pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="0fbd7-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0fbd7-114">-ApplicationName</span></span>
<span data-ttu-id="0fbd7-115">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="0fbd7-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="0fbd7-116">-ApplicationVersion</span></span>
<span data-ttu-id="0fbd7-117">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="0fbd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbd7-118">-DefaultProfile</span></span>
<span data-ttu-id="0fbd7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbd7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbd7-120">-ResourceGroupName</span></span>
<span data-ttu-id="0fbd7-121">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="0fbd7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbd7-122">CommonParameters</span></span>
<span data-ttu-id="0fbd7-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbd7-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0fbd7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbd7-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="0fbd7-125">INPUTS</span></span>

### <span data-ttu-id="0fbd7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0fbd7-126">System.String</span></span>

## <span data-ttu-id="0fbd7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fbd7-127">OUTPUTS</span></span>

### <span data-ttu-id="0fbd7-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="0fbd7-128">System.Void</span></span>

## <span data-ttu-id="0fbd7-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0fbd7-129">NOTES</span></span>

## <span data-ttu-id="0fbd7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fbd7-130">RELATED LINKS</span></span>

[<span data-ttu-id="0fbd7-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0fbd7-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="0fbd7-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0fbd7-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="0fbd7-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0fbd7-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="0fbd7-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="0fbd7-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="0fbd7-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0fbd7-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="0fbd7-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="0fbd7-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


