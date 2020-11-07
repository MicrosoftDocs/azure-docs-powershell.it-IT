---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688528"
---
# <span data-ttu-id="98fc7-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="98fc7-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="98fc7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="98fc7-103">Aggiunge un certificato all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="98fc7-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98fc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98fc7-104">SYNTAX</span></span>

### <span data-ttu-id="98fc7-105">File (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98fc7-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98fc7-106">RawData</span><span class="sxs-lookup"><span data-stu-id="98fc7-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98fc7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98fc7-107">DESCRIPTION</span></span>
<span data-ttu-id="98fc7-108">Il cmdlet **New-AzureBatchCertificate** aggiunge un certificato all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="98fc7-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="98fc7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98fc7-109">EXAMPLES</span></span>

### <span data-ttu-id="98fc7-110">Esempio 1: aggiungere un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="98fc7-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="98fc7-111">Questo comando aggiunge un certificato all'account batch specificato usando il file E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="98fc7-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="98fc7-112">Esempio 2: aggiungere un certificato da dati non elaborati</span><span class="sxs-lookup"><span data-stu-id="98fc7-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="98fc7-113">Il primo comando legge i dati dal file denominato cert. pfx nella variabile $RawData.</span><span class="sxs-lookup"><span data-stu-id="98fc7-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="98fc7-114">Il secondo comando aggiunge un certificato all'account batch specificato usando i dati non elaborati archiviati in $RawData.</span><span class="sxs-lookup"><span data-stu-id="98fc7-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="98fc7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98fc7-115">PARAMETERS</span></span>

### <span data-ttu-id="98fc7-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="98fc7-116">-BatchContext</span></span>
<span data-ttu-id="98fc7-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="98fc7-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98fc7-118">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="98fc7-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="98fc7-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="98fc7-119">-FilePath</span></span>
<span data-ttu-id="98fc7-120">Specifica il percorso del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="98fc7-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="98fc7-121">Il file di certificato deve essere in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="98fc7-121">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="98fc7-122">-Password</span><span class="sxs-lookup"><span data-stu-id="98fc7-122">-Password</span></span>
<span data-ttu-id="98fc7-123">Specifica la password per accedere alla chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="98fc7-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="98fc7-124">È necessario specificare questo parametro se si specifica un certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="98fc7-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98fc7-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="98fc7-125">-RawData</span></span>
<span data-ttu-id="98fc7-126">Specifica i dati del certificato non elaborato in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="98fc7-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="98fc7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fc7-127">-DefaultProfile</span></span>
<span data-ttu-id="98fc7-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98fc7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98fc7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fc7-129">CommonParameters</span></span>
<span data-ttu-id="98fc7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fc7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fc7-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98fc7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fc7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98fc7-132">INPUTS</span></span>

### <span data-ttu-id="98fc7-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98fc7-133">BatchAccountContext</span></span>
<span data-ttu-id="98fc7-134">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="98fc7-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="98fc7-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="98fc7-135">Byte[]</span></span>
<span data-ttu-id="98fc7-136">Il parametro "RawData" accetta il valore di tipo "byte []" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="98fc7-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="98fc7-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98fc7-137">OUTPUTS</span></span>

## <span data-ttu-id="98fc7-138">Note</span><span class="sxs-lookup"><span data-stu-id="98fc7-138">NOTES</span></span>

## <span data-ttu-id="98fc7-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98fc7-139">RELATED LINKS</span></span>

[<span data-ttu-id="98fc7-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="98fc7-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="98fc7-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="98fc7-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="98fc7-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="98fc7-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="98fc7-143">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="98fc7-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


