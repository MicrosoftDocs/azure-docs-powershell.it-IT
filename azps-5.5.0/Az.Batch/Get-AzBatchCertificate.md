---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: 26bd35f59ae5e640093c1695e7caf991e1e1e956
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205331"
---
# <span data-ttu-id="e15e7-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e15e7-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="e15e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e15e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e15e7-103">Recupera i certificati in un account batch.</span><span class="sxs-lookup"><span data-stu-id="e15e7-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="e15e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e15e7-104">SYNTAX</span></span>

### <span data-ttu-id="e15e7-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e15e7-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e15e7-106">Thumbprint</span><span class="sxs-lookup"><span data-stu-id="e15e7-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e15e7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e15e7-107">DESCRIPTION</span></span>
<span data-ttu-id="e15e7-108">Il cmdlet **Get-AzBatchCertificate** ottiene i certificati nell'account batch di Azure specificato dal parametro *BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="e15e7-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="e15e7-109">Per ottenere un certificato specifico, specificare *i parametri ThumbprintAlgorithm* *e Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="e15e7-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="e15e7-110">Specificare il *parametro Filter* per ottenere i certificati corrispondenti a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e15e7-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="e15e7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e15e7-111">EXAMPLES</span></span>

### <span data-ttu-id="e15e7-112">Esempio 1: Ottenere un certificato con l'impronta digitale</span><span class="sxs-lookup"><span data-stu-id="e15e7-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
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

<span data-ttu-id="e15e7-113">Questo comando ottiene un singolo certificato con l'immagine thumbprint specificata.</span><span class="sxs-lookup"><span data-stu-id="e15e7-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="e15e7-114">L'algoritmo per l'impronta digitale del certificato è sha1.</span><span class="sxs-lookup"><span data-stu-id="e15e7-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="e15e7-115">Esempio 2: Ottenere certificati filtrati</span><span class="sxs-lookup"><span data-stu-id="e15e7-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="e15e7-116">Questo comando recupera tutti i certificati nello stato attivo dall'account batch.</span><span class="sxs-lookup"><span data-stu-id="e15e7-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="e15e7-117">Il *parametro Filter* specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="e15e7-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="e15e7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e15e7-118">PARAMETERS</span></span>

### <span data-ttu-id="e15e7-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e15e7-119">-BatchContext</span></span>
<span data-ttu-id="e15e7-120">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e15e7-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e15e7-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e15e7-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e15e7-122">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="e15e7-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e15e7-123">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="e15e7-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e15e7-124">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e15e7-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e15e7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e15e7-125">-DefaultProfile</span></span>
<span data-ttu-id="e15e7-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e15e7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e15e7-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="e15e7-127">-Filter</span></span>
<span data-ttu-id="e15e7-128">Specifica una clausola del filtro OData.</span><span class="sxs-lookup"><span data-stu-id="e15e7-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="e15e7-129">Se si specifica questo parametro, questo cmdlet ottiene i certificati corrispondenti al filtro.</span><span class="sxs-lookup"><span data-stu-id="e15e7-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

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

### <span data-ttu-id="e15e7-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e15e7-130">-MaxCount</span></span>
<span data-ttu-id="e15e7-131">Specifica il numero massimo di certificati da restituire.</span><span class="sxs-lookup"><span data-stu-id="e15e7-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="e15e7-132">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="e15e7-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="e15e7-133">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="e15e7-133">The default value is 1000.</span></span>

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

### <span data-ttu-id="e15e7-134">-Select</span><span class="sxs-lookup"><span data-stu-id="e15e7-134">-Select</span></span>
<span data-ttu-id="e15e7-135">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="e15e7-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="e15e7-136">Specificare un valore per questo parametro per ottenere proprietà specifiche invece di tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e15e7-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="e15e7-137">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="e15e7-137">-Thumbprint</span></span>
<span data-ttu-id="e15e7-138">Specifica l'immagine thumbprint del certificato che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e15e7-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e15e7-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e15e7-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e15e7-140">Specifica l'algoritmo usato per ricavare *il parametro Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="e15e7-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="e15e7-141">Attualmente l'unico valore valido è sha1.</span><span class="sxs-lookup"><span data-stu-id="e15e7-141">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="e15e7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e15e7-142">CommonParameters</span></span>
<span data-ttu-id="e15e7-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e15e7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e15e7-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e15e7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e15e7-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="e15e7-145">INPUTS</span></span>

### <span data-ttu-id="e15e7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e15e7-146">System.String</span></span>

### <span data-ttu-id="e15e7-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e15e7-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e15e7-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e15e7-148">OUTPUTS</span></span>

### <span data-ttu-id="e15e7-149">Microsoft.Azure.Commands.Batch. Models.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="e15e7-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="e15e7-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="e15e7-150">NOTES</span></span>

## <span data-ttu-id="e15e7-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e15e7-151">RELATED LINKS</span></span>

[<span data-ttu-id="e15e7-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e15e7-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e15e7-153">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e15e7-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="e15e7-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e15e7-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="e15e7-155">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="e15e7-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
