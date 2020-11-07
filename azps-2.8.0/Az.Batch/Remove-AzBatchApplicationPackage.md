---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f4b47bb2abab783e4a6995ce57512dbd579e25e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675648"
---
# <span data-ttu-id="3e128-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e128-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="3e128-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e128-102">SYNOPSIS</span></span>
<span data-ttu-id="3e128-103">Elimina un record pacchetto dell'applicazione e il file binario.</span><span class="sxs-lookup"><span data-stu-id="3e128-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="3e128-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e128-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e128-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e128-105">DESCRIPTION</span></span>
<span data-ttu-id="3e128-106">Il cmdlet **Remove-AzBatchApplicationPackage** Elimina un record del pacchetto dell'applicazione e il file binario da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e128-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="3e128-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e128-107">EXAMPLES</span></span>

### <span data-ttu-id="3e128-108">Esempio 1: eliminare un pacchetto di applicazione da un account batch</span><span class="sxs-lookup"><span data-stu-id="3e128-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="3e128-109">Questo comando Elimina la versione 1,0 dell'applicazione Litware dall'account ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="3e128-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="3e128-110">Il comando Elimina sia il record del pacchetto che il BLOB che contengono il file binario del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3e128-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="3e128-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e128-111">PARAMETERS</span></span>

### <span data-ttu-id="3e128-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e128-112">-AccountName</span></span>
<span data-ttu-id="3e128-113">Specifica il nome dell'account batch da cui questo cmdlet elimina un pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e128-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="3e128-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3e128-114">-ApplicationId</span></span>
<span data-ttu-id="3e128-115">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e128-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="3e128-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3e128-116">-ApplicationVersion</span></span>
<span data-ttu-id="3e128-117">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e128-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="3e128-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e128-118">-DefaultProfile</span></span>
<span data-ttu-id="3e128-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e128-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e128-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e128-120">-ResourceGroupName</span></span>
<span data-ttu-id="3e128-121">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="3e128-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="3e128-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e128-122">CommonParameters</span></span>
<span data-ttu-id="3e128-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e128-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e128-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e128-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e128-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e128-125">INPUTS</span></span>

### <span data-ttu-id="3e128-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3e128-126">System.String</span></span>

## <span data-ttu-id="3e128-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e128-127">OUTPUTS</span></span>

### <span data-ttu-id="3e128-128">System. void</span><span class="sxs-lookup"><span data-stu-id="3e128-128">System.Void</span></span>

## <span data-ttu-id="3e128-129">Note</span><span class="sxs-lookup"><span data-stu-id="3e128-129">NOTES</span></span>

## <span data-ttu-id="3e128-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e128-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e128-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e128-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="3e128-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e128-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="3e128-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e128-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="3e128-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e128-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="3e128-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e128-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="3e128-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e128-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


