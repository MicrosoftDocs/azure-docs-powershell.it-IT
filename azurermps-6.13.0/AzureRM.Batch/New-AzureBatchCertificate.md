---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 7038f6c23273153a11aeccc8cbd12fdc6f629c28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513919"
---
# <span data-ttu-id="127a9-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="127a9-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="127a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="127a9-102">SYNOPSIS</span></span>
<span data-ttu-id="127a9-103">Aggiunge un certificato all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="127a9-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="127a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="127a9-104">SYNTAX</span></span>

### <span data-ttu-id="127a9-105">File (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="127a9-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="127a9-106">RawData</span><span class="sxs-lookup"><span data-stu-id="127a9-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="127a9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="127a9-107">DESCRIPTION</span></span>
<span data-ttu-id="127a9-108">Il cmdlet **New-AzureBatchCertificate** aggiunge un certificato all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="127a9-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="127a9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="127a9-109">EXAMPLES</span></span>

### <span data-ttu-id="127a9-110">Esempio 1: aggiungere un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="127a9-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="127a9-111">Questo comando aggiunge un certificato all'account batch specificato usando il file E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="127a9-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="127a9-112">Esempio 2: aggiungere un certificato da dati non elaborati</span><span class="sxs-lookup"><span data-stu-id="127a9-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="127a9-113">Il primo comando legge i dati dal file denominato cert. pfx nella variabile $RawData.</span><span class="sxs-lookup"><span data-stu-id="127a9-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="127a9-114">Il secondo comando aggiunge un certificato all'account batch specificato usando i dati non elaborati archiviati in $RawData.</span><span class="sxs-lookup"><span data-stu-id="127a9-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="127a9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="127a9-115">PARAMETERS</span></span>

### <span data-ttu-id="127a9-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="127a9-116">-BatchContext</span></span>
<span data-ttu-id="127a9-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="127a9-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="127a9-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="127a9-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="127a9-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="127a9-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="127a9-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="127a9-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="127a9-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="127a9-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="127a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127a9-122">-DefaultProfile</span></span>
<span data-ttu-id="127a9-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="127a9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="127a9-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="127a9-124">-FilePath</span></span>
<span data-ttu-id="127a9-125">Specifica il percorso del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="127a9-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="127a9-126">Il file di certificato deve essere in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="127a9-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127a9-127">-Password</span><span class="sxs-lookup"><span data-stu-id="127a9-127">-Password</span></span>
<span data-ttu-id="127a9-128">Specifica la password per accedere alla chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="127a9-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="127a9-129">È necessario specificare questo parametro se si specifica un certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="127a9-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127a9-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="127a9-130">-RawData</span></span>
<span data-ttu-id="127a9-131">Specifica i dati del certificato non elaborato in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="127a9-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="127a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127a9-132">CommonParameters</span></span>
<span data-ttu-id="127a9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127a9-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="127a9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127a9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="127a9-135">INPUTS</span></span>

### <span data-ttu-id="127a9-136">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="127a9-136">System.Byte[]</span></span>

### <span data-ttu-id="127a9-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="127a9-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="127a9-138">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="127a9-138">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="127a9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="127a9-139">OUTPUTS</span></span>

### <span data-ttu-id="127a9-140">System. void</span><span class="sxs-lookup"><span data-stu-id="127a9-140">System.Void</span></span>

## <span data-ttu-id="127a9-141">Note</span><span class="sxs-lookup"><span data-stu-id="127a9-141">NOTES</span></span>

## <span data-ttu-id="127a9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="127a9-142">RELATED LINKS</span></span>

[<span data-ttu-id="127a9-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="127a9-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="127a9-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="127a9-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="127a9-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="127a9-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="127a9-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="127a9-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


