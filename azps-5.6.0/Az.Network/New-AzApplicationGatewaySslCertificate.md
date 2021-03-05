---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 84465161d726108749e09d4a928e22aea8050c92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015054"
---
# <span data-ttu-id="1ef15-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ef15-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1ef15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ef15-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef15-103">Crea un certificato SSL per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef15-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="1ef15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ef15-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ef15-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1ef15-105">DESCRIPTION</span></span>
<span data-ttu-id="1ef15-106">Il cmdlet **New-AzApplicationGatewaySslCertificate** crea un certificato SSL per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef15-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="1ef15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ef15-107">EXAMPLES</span></span>

### <span data-ttu-id="1ef15-108">Esempio 1: Creare un certificato SSL per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef15-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="1ef15-109">Questo comando crea un certificato SSL denominato Cert01 per il gateway applicazione predefinito e archivia il risultato nella variabile $Cert.</span><span class="sxs-lookup"><span data-stu-id="1ef15-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="1ef15-110">Esempio 2: Creare un certificato SSL usando KeyVault Secret (version-less secretId) e aggiungerlo a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ef15-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="1ef15-111">Ottenere il segreto e creare un certificato SSL con `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="1ef15-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="1ef15-112">Nota: poiché l'ID segreto senza versione viene fornito qui, Gateway di applicazione sincronirà il certificato a intervalli regolari con KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1ef15-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="1ef15-113">Esempio 3: Creare un certificato SSL usando il segreto KeyVault e aggiungerlo a un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ef15-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="1ef15-114">Ottenere il segreto e creare un certificato SSL con `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="1ef15-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="1ef15-115">Nota: se è necessario che Gateway applicazioni sincroni il certificato con KeyVault, specificare l'ID secret senza versione.</span><span class="sxs-lookup"><span data-stu-id="1ef15-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="1ef15-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ef15-116">PARAMETERS</span></span>

### <span data-ttu-id="1ef15-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1ef15-117">-CertificateFile</span></span>
<span data-ttu-id="1ef15-118">Specifica il percorso del file PFX del certificato SSL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef15-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1ef15-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef15-119">-DefaultProfile</span></span>
<span data-ttu-id="1ef15-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef15-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ef15-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="1ef15-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="1ef15-122">SecretId (URI) del segreto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1ef15-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="1ef15-123">Usare questa opzione quando è necessario usare una versione specifica del segreto.</span><span class="sxs-lookup"><span data-stu-id="1ef15-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="1ef15-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1ef15-124">-Name</span></span>
<span data-ttu-id="1ef15-125">Specifica il nome del certificato SSL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef15-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef15-126">-Password</span><span class="sxs-lookup"><span data-stu-id="1ef15-126">-Password</span></span>
<span data-ttu-id="1ef15-127">Specifica la password del protocollo SSL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ef15-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1ef15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef15-128">CommonParameters</span></span>
<span data-ttu-id="1ef15-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef15-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef15-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef15-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="1ef15-131">INPUTS</span></span>

### <span data-ttu-id="1ef15-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1ef15-132">None</span></span>

## <span data-ttu-id="1ef15-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ef15-133">OUTPUTS</span></span>

### <span data-ttu-id="1ef15-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ef15-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="1ef15-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="1ef15-135">NOTES</span></span>

## <span data-ttu-id="1ef15-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ef15-136">RELATED LINKS</span></span>

[<span data-ttu-id="1ef15-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ef15-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1ef15-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ef15-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1ef15-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ef15-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="1ef15-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ef15-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


