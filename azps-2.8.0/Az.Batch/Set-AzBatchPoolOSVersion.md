---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865666"
---
# <span data-ttu-id="05a37-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="05a37-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="05a37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05a37-102">SYNOPSIS</span></span>
<span data-ttu-id="05a37-103">Modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="05a37-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="05a37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05a37-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05a37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05a37-105">DESCRIPTION</span></span>
<span data-ttu-id="05a37-106">Il cmdlet **set-AzBatchPoolOSVersion** modifica la versione del sistema operativo del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="05a37-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="05a37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05a37-107">EXAMPLES</span></span>

### <span data-ttu-id="05a37-108">Esempio 1: impostare la versione del sistema operativo di destinazione di un pool</span><span class="sxs-lookup"><span data-stu-id="05a37-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="05a37-109">Questo comando imposta la versione del sistema operativo di destinazione di pool My pool in WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="05a37-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="05a37-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05a37-110">PARAMETERS</span></span>

### <span data-ttu-id="05a37-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="05a37-111">-BatchContext</span></span>
<span data-ttu-id="05a37-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="05a37-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="05a37-113">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="05a37-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="05a37-114">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="05a37-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="05a37-115">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="05a37-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="05a37-116">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="05a37-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="05a37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a37-117">-DefaultProfile</span></span>
<span data-ttu-id="05a37-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05a37-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05a37-119">-ID</span><span class="sxs-lookup"><span data-stu-id="05a37-119">-Id</span></span>
<span data-ttu-id="05a37-120">Specifica l'ID del pool.</span><span class="sxs-lookup"><span data-stu-id="05a37-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="05a37-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="05a37-121">-TargetOSVersion</span></span>
<span data-ttu-id="05a37-122">Specifica la versione del sistema operativo Azure Guest da installare nelle macchine virtuali nel pool.</span><span class="sxs-lookup"><span data-stu-id="05a37-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="05a37-123">Per altre informazioni sulle versioni di Azure Guest System, vedere rilasci del sistema operativo guest Azure e matrice di compatibilità dell'SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="05a37-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="05a37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a37-124">CommonParameters</span></span>
<span data-ttu-id="05a37-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a37-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a37-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a37-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05a37-127">INPUTS</span></span>

### <span data-ttu-id="05a37-128">System. String</span><span class="sxs-lookup"><span data-stu-id="05a37-128">System.String</span></span>

### <span data-ttu-id="05a37-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="05a37-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="05a37-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05a37-130">OUTPUTS</span></span>

### <span data-ttu-id="05a37-131">System. void</span><span class="sxs-lookup"><span data-stu-id="05a37-131">System.Void</span></span>

## <span data-ttu-id="05a37-132">Note</span><span class="sxs-lookup"><span data-stu-id="05a37-132">NOTES</span></span>

## <span data-ttu-id="05a37-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05a37-133">RELATED LINKS</span></span>

[<span data-ttu-id="05a37-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="05a37-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


