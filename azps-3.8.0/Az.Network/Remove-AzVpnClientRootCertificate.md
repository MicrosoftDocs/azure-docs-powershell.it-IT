---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3288573719edac1f04b40ed624820397b4beebcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021908"
---
# <span data-ttu-id="8d3a6-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d3a6-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="8d3a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d3a6-103">Rimuove un certificato radice del client VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="8d3a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d3a6-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d3a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d3a6-105">DESCRIPTION</span></span>
<span data-ttu-id="8d3a6-106">Il cmdlet **Remove-AzVpnClientRootCertificate** rimuove il certificato radice specificato da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="8d3a6-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="8d3a6-108">Se si rimuovono i computer di un certificato radice che usano il certificato per scopi di autenticazione, non sarà più possibile connettersi al gateway.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="8d3a6-109">Quando si usa **Remove-AzVpnClientRootCertificate** , è necessario specificare sia il nome del certificato che una rappresentazione testuale dei dati del certificato.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-109">When you use **Remove-AzVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="8d3a6-110">Per altre informazioni sulla rappresentazione testuale di un certificato, vedere la descrizione del parametro *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="8d3a6-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="8d3a6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d3a6-111">EXAMPLES</span></span>

### <span data-ttu-id="8d3a6-112">Esempio 1: rimuovere un certificato radice client da un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8d3a6-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="8d3a6-113">In questo esempio viene rimosso un certificato radice client denominato ContosoRootCertificate dal gateway di rete virtuale ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="8d3a6-114">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione testuale esportata in precedenza del certificato; Questa rappresentazione di testo è archiviata in una variabile denominata $Text.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="8d3a6-115">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo in $Text tranne che per la prima riga e l'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="8d3a6-116">Questo testo estratto viene archiviato in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="8d3a6-117">Il terzo comando usa le informazioni archiviate nella variabile $CertificateText insieme al cmdlet **Remove-AzVpnClientRootCertificate** per rimuovere il certificato dal gateway.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="8d3a6-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d3a6-118">PARAMETERS</span></span>

### <span data-ttu-id="8d3a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d3a6-119">-DefaultProfile</span></span>
<span data-ttu-id="8d3a6-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d3a6-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="8d3a6-121">-PublicCertData</span></span>
<span data-ttu-id="8d3a6-122">Specifica la rappresentazione testuale del certificato radice da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="8d3a6-123">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (usando Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="8d3a6-124">Dovrebbe essere visualizzato l'output simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato qui):-----iniziare il certificato-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----certificato finale-----PublicCertData è costituito da tutte le linee tra la prima riga (-----iniziare il certificato-----) e l'ultima riga (-----certificato di fine-----) nel file.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="8d3a6-125">Puoi recuperare il PublicCertData usando i comandi di Windows PowerShell in modo simile al seguente: $Text = Get-Content-path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="8d3a6-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d3a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d3a6-127">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="8d3a6-128">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3a6-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8d3a6-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8d3a6-130">Specifica il nome del gateway di rete virtuale da cui viene rimosso il certificato.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3a6-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="8d3a6-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="8d3a6-132">Specifica il nome del certificato radice client rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d3a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d3a6-133">CommonParameters</span></span>
<span data-ttu-id="8d3a6-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d3a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d3a6-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d3a6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d3a6-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d3a6-136">INPUTS</span></span>

### <span data-ttu-id="8d3a6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8d3a6-137">System.String</span></span>

## <span data-ttu-id="8d3a6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d3a6-138">OUTPUTS</span></span>

### <span data-ttu-id="8d3a6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d3a6-139">System.Boolean</span></span>

## <span data-ttu-id="8d3a6-140">Note</span><span class="sxs-lookup"><span data-stu-id="8d3a6-140">NOTES</span></span>

## <span data-ttu-id="8d3a6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d3a6-141">RELATED LINKS</span></span>

[<span data-ttu-id="8d3a6-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d3a6-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="8d3a6-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d3a6-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="8d3a6-144">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8d3a6-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


