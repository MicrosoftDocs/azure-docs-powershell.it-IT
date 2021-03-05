---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 4dde5ab085dede4520b26a4fbeb3255cc62c0fe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982493"
---
# <span data-ttu-id="c0470-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0470-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c0470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0470-102">SYNOPSIS</span></span>
<span data-ttu-id="c0470-103">Aggiunge un certificato SSL a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0470-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="c0470-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0470-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0470-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0470-105">DESCRIPTION</span></span>
<span data-ttu-id="c0470-106">Il cmdlet **Add-AzApplicationGatewaySslCertificate** aggiunge un certificato SSL a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0470-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="c0470-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0470-107">EXAMPLES</span></span>

### <span data-ttu-id="c0470-108">Esempio 1: Aggiungere un certificato SSL usando pfx a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0470-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="c0470-109">Questo comando recupera un gateway applicazione denominato ApplicationGateway01 e quindi aggiunge al gateway un certificato SSL denominato Cert01.</span><span class="sxs-lookup"><span data-stu-id="c0470-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="c0470-110">Esempio 2: Aggiungere un certificato SSL usando KeyVault Secret (version-less secretId) a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0470-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="c0470-111">Ottenere il segreto e fare riferimento a esso in `Add-AzApplicationGatewaySslCertificate` per aggiungerlo al Gateway applicazione con il `Cert01` nome.</span><span class="sxs-lookup"><span data-stu-id="c0470-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="c0470-112">Nota: poiché l'ID segreto senza versione viene fornito qui, Gateway di applicazione sincronirà il certificato a intervalli regolari con KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c0470-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="c0470-113">Esempio 3: Aggiungere un certificato SSL usando KeyVault Secret (versioned secretId) a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0470-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="c0470-114">Ottenere il segreto e fare riferimento a esso in `Add-AzApplicationGatewaySslCertificate` per aggiungerlo al Gateway applicazione con il `Cert01` nome.</span><span class="sxs-lookup"><span data-stu-id="c0470-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="c0470-115">Nota: se è necessario che Gateway applicazioni sincroni il certificato con KeyVault, specificare l'ID segreto senza versione.</span><span class="sxs-lookup"><span data-stu-id="c0470-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="c0470-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0470-116">PARAMETERS</span></span>

### <span data-ttu-id="c0470-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0470-117">-ApplicationGateway</span></span>
<span data-ttu-id="c0470-118">Specifica il nome del gateway applicazione a cui questo cmdlet aggiunge un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="c0470-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="c0470-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="c0470-119">-CertificateFile</span></span>
<span data-ttu-id="c0470-120">Specifica il file PFX di un certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0470-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c0470-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0470-121">-DefaultProfile</span></span>
<span data-ttu-id="c0470-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0470-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0470-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="c0470-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="c0470-124">SecretId (URI) del segreto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c0470-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="c0470-125">Usare questa opzione quando è necessario usare una versione specifica del segreto.</span><span class="sxs-lookup"><span data-stu-id="c0470-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="c0470-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c0470-126">-Name</span></span>
<span data-ttu-id="c0470-127">Specifica il nome del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0470-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c0470-128">-Password</span><span class="sxs-lookup"><span data-stu-id="c0470-128">-Password</span></span>
<span data-ttu-id="c0470-129">Specifica la password del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0470-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c0470-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0470-130">CommonParameters</span></span>
<span data-ttu-id="c0470-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0470-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0470-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0470-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0470-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0470-133">INPUTS</span></span>

### <span data-ttu-id="c0470-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0470-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0470-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0470-135">OUTPUTS</span></span>

### <span data-ttu-id="c0470-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0470-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0470-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0470-137">NOTES</span></span>

## <span data-ttu-id="c0470-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0470-138">RELATED LINKS</span></span>

[<span data-ttu-id="c0470-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0470-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c0470-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0470-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c0470-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0470-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c0470-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c0470-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


