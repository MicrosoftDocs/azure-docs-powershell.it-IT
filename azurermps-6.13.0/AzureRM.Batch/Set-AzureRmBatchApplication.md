---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 8ede896e6a49cee5305e7f9fd42f6dab130e7986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517560"
---
# <span data-ttu-id="db780-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="db780-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="db780-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db780-102">SYNOPSIS</span></span>
<span data-ttu-id="db780-103">Aggiorna le impostazioni per l'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="db780-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db780-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db780-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db780-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db780-105">DESCRIPTION</span></span>
<span data-ttu-id="db780-106">Il cmdlet **set-AzureRmBatchApplication** modifica le impostazioni per l'applicazione batch Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="db780-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="db780-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db780-107">EXAMPLES</span></span>

### <span data-ttu-id="db780-108">Esempio 1: aggiornare un'applicazione in un account batch</span><span class="sxs-lookup"><span data-stu-id="db780-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="db780-109">Questo comando cambia se l'applicazione Llitware nell'account ContosoBatch consente gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="db780-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="db780-110">Il comando non modifica la versione predefinita o il nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="db780-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="db780-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db780-111">PARAMETERS</span></span>

### <span data-ttu-id="db780-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="db780-112">-AccountName</span></span>
<span data-ttu-id="db780-113">Specifica il nome dell'account batch per cui questo cmdlet modifica un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="db780-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="db780-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="db780-114">-AllowUpdates</span></span>
<span data-ttu-id="db780-115">Specifica se i pacchetti all'interno dell'applicazione possono essere sovrascritti usando la stessa stringa di versione.</span><span class="sxs-lookup"><span data-stu-id="db780-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db780-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="db780-116">-ApplicationId</span></span>
<span data-ttu-id="db780-117">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="db780-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="db780-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db780-118">-DefaultProfile</span></span>
<span data-ttu-id="db780-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db780-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db780-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="db780-120">-DefaultVersion</span></span>
<span data-ttu-id="db780-121">Specifica il pacchetto da usare se un client richiede l'applicazione ma non specifica una versione.</span><span class="sxs-lookup"><span data-stu-id="db780-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="db780-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db780-122">-DisplayName</span></span>
<span data-ttu-id="db780-123">Specifica il nome visualizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="db780-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="db780-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db780-124">-ResourceGroupName</span></span>
<span data-ttu-id="db780-125">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="db780-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="db780-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db780-126">CommonParameters</span></span>
<span data-ttu-id="db780-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db780-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db780-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db780-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db780-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db780-129">INPUTS</span></span>

### <span data-ttu-id="db780-130">System. String</span><span class="sxs-lookup"><span data-stu-id="db780-130">System.String</span></span>

### <span data-ttu-id="db780-131">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="db780-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="db780-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db780-132">OUTPUTS</span></span>

### <span data-ttu-id="db780-133">System. void</span><span class="sxs-lookup"><span data-stu-id="db780-133">System.Void</span></span>

## <span data-ttu-id="db780-134">Note</span><span class="sxs-lookup"><span data-stu-id="db780-134">NOTES</span></span>

## <span data-ttu-id="db780-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db780-135">RELATED LINKS</span></span>

[<span data-ttu-id="db780-136">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="db780-136">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="db780-137">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="db780-137">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="db780-138">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="db780-138">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="db780-139">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="db780-139">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="db780-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="db780-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="db780-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="db780-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


