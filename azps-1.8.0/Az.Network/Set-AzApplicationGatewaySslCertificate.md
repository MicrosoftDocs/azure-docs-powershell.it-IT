---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 36f45cc5c49cbdf3183f34068fd5b87000c1ede5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677992"
---
# <span data-ttu-id="0c657-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0c657-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0c657-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c657-102">SYNOPSIS</span></span>
<span data-ttu-id="0c657-103">Aggiorna un certificato SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c657-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="0c657-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c657-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c657-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c657-105">DESCRIPTION</span></span>
<span data-ttu-id="0c657-106">Il cmdlet **set-AzApplicationGatewaySslCertificate** aggiorna un certificato SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c657-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="0c657-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c657-107">EXAMPLES</span></span>

### <span data-ttu-id="0c657-108">Esempio 1: aggiornare un certificato SSL esistente nel gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="0c657-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="0c657-109">Aggiornare un certificato SSL esistente per il gateway dell'applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="0c657-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="0c657-110">Esempio 2: aggiornare un certificato SSL esistente tramite il gateway segreto di archiviazione (versione meno secretId) nel portale dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="0c657-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0c657-111">Ottenere il segreto e aggiornare un certificato SSL esistente in uso `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="0c657-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="0c657-112">Esempio 3: aggiornare un certificato SSL esistente tramite la password di accesso al gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="0c657-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0c657-113">Ottenere il segreto e aggiornare un certificato SSL esistente in uso `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="0c657-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="0c657-114">Nota: se è necessario che il gateway dell'applicazione sincronizza il certificato con il Vault, fornisci la versione meno secretId.</span><span class="sxs-lookup"><span data-stu-id="0c657-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="0c657-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c657-115">PARAMETERS</span></span>

### <span data-ttu-id="0c657-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c657-116">-ApplicationGateway</span></span>
<span data-ttu-id="0c657-117">Specifica il gateway dell'applicazione a cui è associato il certificato SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="0c657-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c657-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0c657-118">-CertificateFile</span></span>
<span data-ttu-id="0c657-119">Specifica il percorso del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="0c657-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="0c657-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c657-120">-DefaultProfile</span></span>
<span data-ttu-id="0c657-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c657-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c657-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="0c657-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="0c657-123">SecretId (URI) del segreto del Vault.</span><span class="sxs-lookup"><span data-stu-id="0c657-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="0c657-124">Usa questa opzione quando è necessario usare una specifica versione di segreto.</span><span class="sxs-lookup"><span data-stu-id="0c657-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="0c657-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c657-125">-Name</span></span>
<span data-ttu-id="0c657-126">Specifica il nome del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="0c657-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="0c657-127">-Password</span><span class="sxs-lookup"><span data-stu-id="0c657-127">-Password</span></span>
<span data-ttu-id="0c657-128">Specifica la password del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="0c657-128">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="0c657-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c657-129">CommonParameters</span></span>
<span data-ttu-id="0c657-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c657-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c657-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c657-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c657-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c657-132">INPUTS</span></span>

### <span data-ttu-id="0c657-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c657-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c657-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c657-134">OUTPUTS</span></span>

### <span data-ttu-id="0c657-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c657-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c657-136">Note</span><span class="sxs-lookup"><span data-stu-id="0c657-136">NOTES</span></span>

## <span data-ttu-id="0c657-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c657-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c657-138">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0c657-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0c657-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0c657-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0c657-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0c657-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0c657-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0c657-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


