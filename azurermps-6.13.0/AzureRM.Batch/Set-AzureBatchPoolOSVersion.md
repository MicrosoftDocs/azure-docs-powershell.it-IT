---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: d85e0ca61b86e523c6d73ea8d2349d7d692aafb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519761"
---
# <span data-ttu-id="01f11-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="01f11-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="01f11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01f11-102">SYNOPSIS</span></span>
<span data-ttu-id="01f11-103">Modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="01f11-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01f11-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01f11-105">DESCRIPTION</span></span>
<span data-ttu-id="01f11-106">Il cmdlet **set-AzureBatchPoolOSVersion** modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="01f11-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="01f11-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01f11-107">EXAMPLES</span></span>

### <span data-ttu-id="01f11-108">Esempio 1: impostare la versione del sistema operativo di destinazione di un pool</span><span class="sxs-lookup"><span data-stu-id="01f11-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="01f11-109">Questo comando imposta la versione del sistema operativo di destinazione di pool My pool in WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="01f11-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="01f11-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01f11-110">PARAMETERS</span></span>

### <span data-ttu-id="01f11-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="01f11-111">-BatchContext</span></span>
<span data-ttu-id="01f11-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="01f11-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="01f11-113">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="01f11-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="01f11-114">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="01f11-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="01f11-115">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="01f11-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="01f11-116">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="01f11-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="01f11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f11-117">-DefaultProfile</span></span>
<span data-ttu-id="01f11-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01f11-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01f11-119">-ID</span><span class="sxs-lookup"><span data-stu-id="01f11-119">-Id</span></span>
<span data-ttu-id="01f11-120">Specifica l'ID del pool.</span><span class="sxs-lookup"><span data-stu-id="01f11-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="01f11-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="01f11-121">-TargetOSVersion</span></span>
<span data-ttu-id="01f11-122">Specifica la versione del sistema operativo Azure Guest da installare nelle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="01f11-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="01f11-123">Per altre informazioni sulle versioni di Azure Guest System, vedere rilasci del sistema operativo guest Azure e matrice di compatibilità dell'SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="01f11-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="01f11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f11-124">CommonParameters</span></span>
<span data-ttu-id="01f11-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f11-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f11-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f11-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01f11-127">INPUTS</span></span>

### <span data-ttu-id="01f11-128">System. String</span><span class="sxs-lookup"><span data-stu-id="01f11-128">System.String</span></span>

### <span data-ttu-id="01f11-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="01f11-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="01f11-130">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01f11-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="01f11-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01f11-131">OUTPUTS</span></span>

### <span data-ttu-id="01f11-132">System. void</span><span class="sxs-lookup"><span data-stu-id="01f11-132">System.Void</span></span>

## <span data-ttu-id="01f11-133">Note</span><span class="sxs-lookup"><span data-stu-id="01f11-133">NOTES</span></span>

## <span data-ttu-id="01f11-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01f11-134">RELATED LINKS</span></span>

[<span data-ttu-id="01f11-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="01f11-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


