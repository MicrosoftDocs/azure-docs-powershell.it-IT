---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520697"
---
# <span data-ttu-id="12b1b-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="12b1b-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="12b1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="12b1b-103">Modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="12b1b-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12b1b-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12b1b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="12b1b-106">Il cmdlet **set-AzureBatchPoolOSVersion** modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="12b1b-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="12b1b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12b1b-107">EXAMPLES</span></span>

### <span data-ttu-id="12b1b-108">Esempio 1: impostare la versione del sistema operativo di destinazione di un pool</span><span class="sxs-lookup"><span data-stu-id="12b1b-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="12b1b-109">Questo comando imposta la versione del sistema operativo di destinazione di pool My pool in WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="12b1b-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="12b1b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12b1b-110">PARAMETERS</span></span>

### <span data-ttu-id="12b1b-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="12b1b-111">-BatchContext</span></span>
<span data-ttu-id="12b1b-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="12b1b-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="12b1b-113">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="12b1b-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="12b1b-114">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="12b1b-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="12b1b-115">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="12b1b-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="12b1b-116">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="12b1b-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12b1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b1b-117">-DefaultProfile</span></span>
<span data-ttu-id="12b1b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12b1b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b1b-119">-ID</span><span class="sxs-lookup"><span data-stu-id="12b1b-119">-Id</span></span>
<span data-ttu-id="12b1b-120">Specifica l'ID del pool.</span><span class="sxs-lookup"><span data-stu-id="12b1b-120">Specifies the ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12b1b-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="12b1b-121">-TargetOSVersion</span></span>
<span data-ttu-id="12b1b-122">Specifica la versione del sistema operativo Azure Guest da installare nelle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="12b1b-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="12b1b-123">Per altre informazioni sulle versioni di Azure Guest System, vedere rilasci del sistema operativo guest Azure e matrice di compatibilità dell'SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="12b1b-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b1b-124">CommonParameters</span></span>
<span data-ttu-id="12b1b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b1b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b1b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b1b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12b1b-127">INPUTS</span></span>

### <span data-ttu-id="12b1b-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="12b1b-128">BatchAccountContext</span></span>
<span data-ttu-id="12b1b-129">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="12b1b-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="12b1b-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="12b1b-130">String</span></span>
<span data-ttu-id="12b1b-131">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="12b1b-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="12b1b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12b1b-132">OUTPUTS</span></span>

## <span data-ttu-id="12b1b-133">Note</span><span class="sxs-lookup"><span data-stu-id="12b1b-133">NOTES</span></span>

## <span data-ttu-id="12b1b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12b1b-134">RELATED LINKS</span></span>

[<span data-ttu-id="12b1b-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="12b1b-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


