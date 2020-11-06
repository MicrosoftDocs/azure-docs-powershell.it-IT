---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521933"
---
# <span data-ttu-id="b903b-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b903b-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="b903b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b903b-102">SYNOPSIS</span></span>
<span data-ttu-id="b903b-103">Aggiunge un certificato all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="b903b-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b903b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b903b-104">SYNTAX</span></span>

### <span data-ttu-id="b903b-105">File (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b903b-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b903b-106">RawData</span><span class="sxs-lookup"><span data-stu-id="b903b-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b903b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b903b-107">DESCRIPTION</span></span>
<span data-ttu-id="b903b-108">Il cmdlet **New-AzureBatchCertificate** aggiunge un certificato all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="b903b-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="b903b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b903b-109">EXAMPLES</span></span>

### <span data-ttu-id="b903b-110">Esempio 1: aggiungere un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="b903b-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="b903b-111">Questo comando aggiunge un certificato all'account batch specificato usando il file E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="b903b-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="b903b-112">Esempio 2: aggiungere un certificato da dati non elaborati</span><span class="sxs-lookup"><span data-stu-id="b903b-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="b903b-113">Il primo comando legge i dati dal file denominato cert. pfx nella variabile $RawData.</span><span class="sxs-lookup"><span data-stu-id="b903b-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="b903b-114">Il secondo comando aggiunge un certificato all'account batch specificato usando i dati non elaborati archiviati in $RawData.</span><span class="sxs-lookup"><span data-stu-id="b903b-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="b903b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b903b-115">PARAMETERS</span></span>

### <span data-ttu-id="b903b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b903b-116">-BatchContext</span></span>
<span data-ttu-id="b903b-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b903b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b903b-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b903b-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b903b-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="b903b-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b903b-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b903b-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b903b-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b903b-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b903b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b903b-122">-DefaultProfile</span></span>
<span data-ttu-id="b903b-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b903b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b903b-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b903b-124">-FilePath</span></span>
<span data-ttu-id="b903b-125">Specifica il percorso del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="b903b-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="b903b-126">Il file di certificato deve essere in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="b903b-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b903b-127">-Password</span><span class="sxs-lookup"><span data-stu-id="b903b-127">-Password</span></span>
<span data-ttu-id="b903b-128">Specifica la password per accedere alla chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="b903b-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="b903b-129">È necessario specificare questo parametro se si specifica un certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="b903b-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b903b-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="b903b-130">-RawData</span></span>
<span data-ttu-id="b903b-131">Specifica i dati del certificato non elaborato in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="b903b-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b903b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b903b-132">CommonParameters</span></span>
<span data-ttu-id="b903b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b903b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b903b-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b903b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b903b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b903b-135">INPUTS</span></span>

### <span data-ttu-id="b903b-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b903b-136">BatchAccountContext</span></span>
<span data-ttu-id="b903b-137">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b903b-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b903b-138">Byte []</span><span class="sxs-lookup"><span data-stu-id="b903b-138">Byte[]</span></span>
<span data-ttu-id="b903b-139">Il parametro "RawData" accetta il valore di tipo "byte []" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b903b-139">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="b903b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b903b-140">OUTPUTS</span></span>

## <span data-ttu-id="b903b-141">Note</span><span class="sxs-lookup"><span data-stu-id="b903b-141">NOTES</span></span>

## <span data-ttu-id="b903b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b903b-142">RELATED LINKS</span></span>

[<span data-ttu-id="b903b-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b903b-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="b903b-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b903b-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b903b-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b903b-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="b903b-146">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b903b-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


