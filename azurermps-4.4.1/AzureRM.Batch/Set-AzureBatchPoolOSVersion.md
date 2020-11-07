---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686868"
---
# <span data-ttu-id="0d028-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="0d028-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="0d028-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d028-102">SYNOPSIS</span></span>
<span data-ttu-id="0d028-103">Modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="0d028-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d028-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d028-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d028-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d028-105">DESCRIPTION</span></span>
<span data-ttu-id="0d028-106">Il cmdlet **set-AzureBatchPoolOSVersion** modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="0d028-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="0d028-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d028-107">EXAMPLES</span></span>

### <span data-ttu-id="0d028-108">Esempio 1: impostare la versione del sistema operativo di destinazione di un pool</span><span class="sxs-lookup"><span data-stu-id="0d028-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="0d028-109">Questo comando imposta la versione del sistema operativo di destinazione di pool My pool in WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="0d028-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="0d028-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d028-110">PARAMETERS</span></span>

### <span data-ttu-id="0d028-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0d028-111">-BatchContext</span></span>
<span data-ttu-id="0d028-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0d028-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0d028-113">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="0d028-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d028-114">-ID</span><span class="sxs-lookup"><span data-stu-id="0d028-114">-Id</span></span>
<span data-ttu-id="0d028-115">Specifica l'ID del pool.</span><span class="sxs-lookup"><span data-stu-id="0d028-115">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d028-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="0d028-116">-TargetOSVersion</span></span>
<span data-ttu-id="0d028-117">Specifica la versione del sistema operativo Azure Guest da installare nelle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="0d028-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="0d028-118">Per altre informazioni sulle versioni di Azure Guest System, vedere rilasci del sistema operativo guest Azure e matrice di compatibilità dell'SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="0d028-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d028-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d028-119">-DefaultProfile</span></span>
<span data-ttu-id="0d028-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d028-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d028-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d028-121">CommonParameters</span></span>
<span data-ttu-id="0d028-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d028-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d028-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d028-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d028-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d028-124">INPUTS</span></span>

### <span data-ttu-id="0d028-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0d028-125">BatchAccountContext</span></span>
<span data-ttu-id="0d028-126">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0d028-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0d028-127">Stringa</span><span class="sxs-lookup"><span data-stu-id="0d028-127">String</span></span>
<span data-ttu-id="0d028-128">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0d028-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0d028-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d028-129">OUTPUTS</span></span>

## <span data-ttu-id="0d028-130">Note</span><span class="sxs-lookup"><span data-stu-id="0d028-130">NOTES</span></span>

## <span data-ttu-id="0d028-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d028-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d028-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0d028-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


