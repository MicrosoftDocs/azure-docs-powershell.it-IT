---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
ms.openlocfilehash: c78cf87d4e68c4a9e1b896235d85dde9e8458f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517588"
---
# <span data-ttu-id="92f1c-101">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="92f1c-101">Get-AzureBatchCertificate</span></span>

## <span data-ttu-id="92f1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="92f1c-103">Ottiene i certificati in un account batch.</span><span class="sxs-lookup"><span data-stu-id="92f1c-103">Gets the certificates in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92f1c-104">SYNTAX</span></span>

### <span data-ttu-id="92f1c-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92f1c-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f1c-106">Thumbprint</span><span class="sxs-lookup"><span data-stu-id="92f1c-106">Thumbprint</span></span>
```
Get-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f1c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92f1c-107">DESCRIPTION</span></span>
<span data-ttu-id="92f1c-108">Il cmdlet **Get-AzureBatchCertificate** ottiene i certificati nell'account batch di Azure specificato dal parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="92f1c-108">The **Get-AzureBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="92f1c-109">Per ottenere un determinato certificato, specificare i parametri *ThumbprintAlgorithm* e *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="92f1c-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="92f1c-110">Specifica il parametro *Filter* per ottenere i certificati che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="92f1c-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="92f1c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92f1c-111">EXAMPLES</span></span>

### <span data-ttu-id="92f1c-112">Esempio 1: ottenere un certificato per identificazione personale</span><span class="sxs-lookup"><span data-stu-id="92f1c-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzureBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="92f1c-113">Questo comando ottiene un singolo certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="92f1c-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="92f1c-114">L'algoritmo di identificazione personale del certificato è SHA1.</span><span class="sxs-lookup"><span data-stu-id="92f1c-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="92f1c-115">Esempio 2: ottenere certificati filtrati</span><span class="sxs-lookup"><span data-stu-id="92f1c-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      : 

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="92f1c-116">Questo comando consente di ottenere tutti i certificati nello stato attivo dall'account batch.</span><span class="sxs-lookup"><span data-stu-id="92f1c-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="92f1c-117">Il parametro *Filter* specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="92f1c-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="92f1c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92f1c-118">PARAMETERS</span></span>

### <span data-ttu-id="92f1c-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="92f1c-119">-BatchContext</span></span>
<span data-ttu-id="92f1c-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="92f1c-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="92f1c-121">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="92f1c-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="92f1c-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="92f1c-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="92f1c-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="92f1c-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="92f1c-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="92f1c-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="92f1c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f1c-125">-DefaultProfile</span></span>
<span data-ttu-id="92f1c-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92f1c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f1c-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="92f1c-127">-Filter</span></span>
<span data-ttu-id="92f1c-128">Specifica una clausola di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="92f1c-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="92f1c-129">Se specifichi questo parametro, questo cmdlet ottiene i certificati che corrispondono al filtro.</span><span class="sxs-lookup"><span data-stu-id="92f1c-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1c-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="92f1c-130">-MaxCount</span></span>
<span data-ttu-id="92f1c-131">Specifica il numero massimo di certificati da restituire.</span><span class="sxs-lookup"><span data-stu-id="92f1c-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="92f1c-132">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="92f1c-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="92f1c-133">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="92f1c-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f1c-134">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="92f1c-134">-Select</span></span>
<span data-ttu-id="92f1c-135">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="92f1c-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="92f1c-136">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="92f1c-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="92f1c-137">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="92f1c-137">-Thumbprint</span></span>
<span data-ttu-id="92f1c-138">Specifica l'identificazione personale del certificato ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92f1c-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f1c-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="92f1c-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="92f1c-140">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="92f1c-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="92f1c-141">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="92f1c-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f1c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f1c-142">CommonParameters</span></span>
<span data-ttu-id="92f1c-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f1c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f1c-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f1c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f1c-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92f1c-145">INPUTS</span></span>

### <span data-ttu-id="92f1c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="92f1c-146">System.String</span></span>

### <span data-ttu-id="92f1c-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="92f1c-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="92f1c-148">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92f1c-148">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="92f1c-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92f1c-149">OUTPUTS</span></span>

### <span data-ttu-id="92f1c-150">Microsoft.Azure.Commands.Batch. Models. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="92f1c-150">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="92f1c-151">Note</span><span class="sxs-lookup"><span data-stu-id="92f1c-151">NOTES</span></span>

## <span data-ttu-id="92f1c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92f1c-152">RELATED LINKS</span></span>

[<span data-ttu-id="92f1c-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="92f1c-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="92f1c-154">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="92f1c-154">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="92f1c-155">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="92f1c-155">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="92f1c-156">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="92f1c-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


