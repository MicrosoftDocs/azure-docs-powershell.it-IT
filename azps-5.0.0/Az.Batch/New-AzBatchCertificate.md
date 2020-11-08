---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199883"
---
# <span data-ttu-id="9d73a-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9d73a-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="9d73a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d73a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d73a-103">Aggiunge un certificato all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="9d73a-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="9d73a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d73a-104">SYNTAX</span></span>

### <span data-ttu-id="9d73a-105">File (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d73a-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d73a-106">RawData</span><span class="sxs-lookup"><span data-stu-id="9d73a-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d73a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d73a-107">DESCRIPTION</span></span>
<span data-ttu-id="9d73a-108">Il cmdlet **New-AzBatchCertificate** aggiunge un certificato all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="9d73a-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="9d73a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d73a-109">EXAMPLES</span></span>

### <span data-ttu-id="9d73a-110">Esempio 1: aggiungere un certificato da un file</span><span class="sxs-lookup"><span data-stu-id="9d73a-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="9d73a-111">Questo comando aggiunge un certificato all'account batch specificato usando il file E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="9d73a-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="9d73a-112">Esempio 2: aggiungere un certificato da dati non elaborati</span><span class="sxs-lookup"><span data-stu-id="9d73a-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="9d73a-113">Il primo comando legge i dati dal file denominato cert. pfx nella variabile $RawData.</span><span class="sxs-lookup"><span data-stu-id="9d73a-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="9d73a-114">Il secondo comando aggiunge un certificato all'account batch specificato usando i dati non elaborati archiviati in $RawData.</span><span class="sxs-lookup"><span data-stu-id="9d73a-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="9d73a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d73a-115">PARAMETERS</span></span>

### <span data-ttu-id="9d73a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9d73a-116">-BatchContext</span></span>
<span data-ttu-id="9d73a-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="9d73a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9d73a-118">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="9d73a-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9d73a-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="9d73a-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9d73a-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9d73a-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9d73a-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9d73a-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9d73a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d73a-122">-DefaultProfile</span></span>
<span data-ttu-id="9d73a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d73a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d73a-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9d73a-124">-FilePath</span></span>
<span data-ttu-id="9d73a-125">Specifica il percorso del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="9d73a-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="9d73a-126">Il file di certificato deve essere in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="9d73a-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="9d73a-127">-Tipo</span><span class="sxs-lookup"><span data-stu-id="9d73a-127">-Kind</span></span>
<span data-ttu-id="9d73a-128">Tipo di certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="9d73a-128">The kind of certificate to create.</span></span> <span data-ttu-id="9d73a-129">Se non viene specificato, viene considerato che tutti i certificati senza password sono CER e tutti i certificati con password sono PFX.</span><span class="sxs-lookup"><span data-stu-id="9d73a-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d73a-130">-Password</span><span class="sxs-lookup"><span data-stu-id="9d73a-130">-Password</span></span>
<span data-ttu-id="9d73a-131">Specifica la password per accedere alla chiave privata del certificato.</span><span class="sxs-lookup"><span data-stu-id="9d73a-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="9d73a-132">È necessario specificare questo parametro se si specifica un certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="9d73a-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="9d73a-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="9d73a-133">-RawData</span></span>
<span data-ttu-id="9d73a-134">Specifica i dati del certificato non elaborato in formato CER o PFX.</span><span class="sxs-lookup"><span data-stu-id="9d73a-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="9d73a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d73a-135">CommonParameters</span></span>
<span data-ttu-id="9d73a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d73a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d73a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d73a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d73a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d73a-138">INPUTS</span></span>

### <span data-ttu-id="9d73a-139">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="9d73a-139">System.Byte[]</span></span>

### <span data-ttu-id="9d73a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9d73a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9d73a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d73a-141">OUTPUTS</span></span>

### <span data-ttu-id="9d73a-142">System. void</span><span class="sxs-lookup"><span data-stu-id="9d73a-142">System.Void</span></span>

## <span data-ttu-id="9d73a-143">Note</span><span class="sxs-lookup"><span data-stu-id="9d73a-143">NOTES</span></span>

## <span data-ttu-id="9d73a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d73a-144">RELATED LINKS</span></span>

[<span data-ttu-id="9d73a-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9d73a-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="9d73a-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9d73a-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9d73a-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9d73a-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="9d73a-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="9d73a-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
