---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 75d86c77b57511b5a3fefb9cc21a668a81446746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685896"
---
# <span data-ttu-id="3449e-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3449e-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="3449e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3449e-102">SYNOPSIS</span></span>
<span data-ttu-id="3449e-103">Rimuove un certificato radice del client VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="3449e-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3449e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3449e-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3449e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3449e-105">DESCRIPTION</span></span>
<span data-ttu-id="3449e-106">Il cmdlet **Remove-AzureRmVpnClientRootCertificate** rimuove il certificato radice specificato da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3449e-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="3449e-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="3449e-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="3449e-108">Se si rimuovono i computer di un certificato radice che usano il certificato per scopi di autenticazione, non sarà più possibile connettersi al gateway.</span><span class="sxs-lookup"><span data-stu-id="3449e-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>

<span data-ttu-id="3449e-109">Quando si usa **Remove-AzureRmVpnClientRootCertificate** , è necessario specificare sia il nome del certificato che una rappresentazione testuale dei dati del certificato.</span><span class="sxs-lookup"><span data-stu-id="3449e-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="3449e-110">Per altre informazioni sulla rappresentazione testuale di un certificato, vedere la descrizione del parametro *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="3449e-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="3449e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3449e-111">EXAMPLES</span></span>

### <span data-ttu-id="3449e-112">Esempio 1: rimuovere un certificato radice client da un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3449e-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="3449e-113">In questo esempio viene rimosso un certificato radice client denominato ContosoRootCertificate dal gateway di rete virtuale ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="3449e-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>

<span data-ttu-id="3449e-114">Il primo comando usa il cmdlet **Get-Content** per ottenere una rappresentazione testuale esportata in precedenza del certificato; Questa rappresentazione di testo è archiviata in una variabile denominata $Text.</span><span class="sxs-lookup"><span data-stu-id="3449e-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>

<span data-ttu-id="3449e-115">Il secondo comando usa quindi un ciclo for per estrarre tutto il testo in $Text tranne che per la prima riga e l'ultima riga.</span><span class="sxs-lookup"><span data-stu-id="3449e-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="3449e-116">Questo testo estratto viene archiviato in una variabile denominata $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="3449e-116">This extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="3449e-117">Il terzo comando usa le informazioni archiviate nella variabile $CertificateText insieme al cmdlet **Remove-AzureRmVpnClientRootCertificate** per rimuovere il certificato dal gateway.</span><span class="sxs-lookup"><span data-stu-id="3449e-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="3449e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3449e-118">PARAMETERS</span></span>

### <span data-ttu-id="3449e-119">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="3449e-119">-PublicCertData</span></span>
<span data-ttu-id="3449e-120">Specifica la rappresentazione testuale del certificato radice da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3449e-120">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="3449e-121">Per ottenere la rappresentazione di testo, esportare il certificato in formato CER (usando Base64), quindi aprire il file risultante in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="3449e-121">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="3449e-122">Dovrebbe essere visualizzato l'output simile al seguente (si noti che l'output effettivo conterrà molte più righe di testo rispetto all'esempio abbreviato illustrato qui):</span><span class="sxs-lookup"><span data-stu-id="3449e-122">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="3449e-123">-----INIZIARE il certificato-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----certificato finale-----</span><span class="sxs-lookup"><span data-stu-id="3449e-123">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="3449e-124">PublicCertData è costituito da tutte le linee tra la prima riga (-----iniziare il certificato-----) e l'ultima riga (----------certificato finale) nel file.</span><span class="sxs-lookup"><span data-stu-id="3449e-124">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="3449e-125">Puoi recuperare PublicCertData usando i comandi di Windows PowerShell in modo simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="3449e-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="3449e-126">$Text = Get-Content-path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="3449e-126">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="3449e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3449e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3449e-128">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3449e-128">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="3449e-129">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3449e-129">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="3449e-130">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3449e-130">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3449e-131">Specifica il nome del gateway di rete virtuale da cui viene rimosso il certificato.</span><span class="sxs-lookup"><span data-stu-id="3449e-131">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="3449e-132">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="3449e-132">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="3449e-133">Specifica il nome del certificato radice client rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3449e-133">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3449e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3449e-134">-DefaultProfile</span></span>
<span data-ttu-id="3449e-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3449e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3449e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3449e-136">CommonParameters</span></span>
<span data-ttu-id="3449e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3449e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3449e-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3449e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3449e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3449e-139">INPUTS</span></span>

## <span data-ttu-id="3449e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3449e-140">OUTPUTS</span></span>

## <span data-ttu-id="3449e-141">Note</span><span class="sxs-lookup"><span data-stu-id="3449e-141">NOTES</span></span>

## <span data-ttu-id="3449e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3449e-142">RELATED LINKS</span></span>

[<span data-ttu-id="3449e-143">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3449e-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="3449e-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3449e-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="3449e-145">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3449e-145">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)


