---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 6939f26dc06e0aa5ed56d3e905d30960094e8961
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207050"
---
# <span data-ttu-id="81d89-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81d89-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="81d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d89-102">SYNOPSIS</span></span>
<span data-ttu-id="81d89-103">Aggiunge un certificato SSL a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="81d89-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="81d89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81d89-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d89-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="81d89-105">DESCRIPTION</span></span>
<span data-ttu-id="81d89-106">Il cmdlet **Add-AzApplicationGatewaySslCertificate** aggiunge un certificato SSL a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="81d89-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="81d89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81d89-107">EXAMPLES</span></span>

### <span data-ttu-id="81d89-108">Esempio 1: Aggiungere un certificato SSL usando pfx a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="81d89-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="81d89-109">Questo comando recupera un gateway applicazione denominato ApplicationGateway01 e quindi aggiunge al gateway un certificato SSL denominato Cert01.</span><span class="sxs-lookup"><span data-stu-id="81d89-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="81d89-110">Esempio 2: Aggiungere un certificato SSL usando KeyVault Secret (version-less secretId) a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="81d89-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="81d89-111">Ottenere il segreto e fare riferimento a esso in `Add-AzApplicationGatewaySslCertificate` per aggiungerlo al Gateway applicazione con il `Cert01` nome.</span><span class="sxs-lookup"><span data-stu-id="81d89-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="81d89-112">Nota: poiché l'ID segreto senza versione viene specificato qui, Gateway di applicazione sincronirà il certificato a intervalli regolari con KeyVault.</span><span class="sxs-lookup"><span data-stu-id="81d89-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="81d89-113">Esempio 3: Aggiungere un certificato SSL usando KeyVault Secret (versioned secretId) a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="81d89-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="81d89-114">Ottenere il segreto e fare riferimento a esso in `Add-AzApplicationGatewaySslCertificate` per aggiungerlo al Gateway applicazione con il `Cert01` nome.</span><span class="sxs-lookup"><span data-stu-id="81d89-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="81d89-115">Nota: se è necessario che Gateway applicazioni sincroni il certificato con KeyVault, specificare l'ID segreto senza versione.</span><span class="sxs-lookup"><span data-stu-id="81d89-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="81d89-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81d89-116">PARAMETERS</span></span>

### <span data-ttu-id="81d89-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81d89-117">-ApplicationGateway</span></span>
<span data-ttu-id="81d89-118">Specifica il nome del gateway applicazione a cui questo cmdlet aggiunge un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="81d89-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="81d89-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="81d89-119">-CertificateFile</span></span>
<span data-ttu-id="81d89-120">Specifica il file PFX di un certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d89-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="81d89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d89-121">-DefaultProfile</span></span>
<span data-ttu-id="81d89-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81d89-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d89-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="81d89-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="81d89-124">SecretId (URI) del segreto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="81d89-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="81d89-125">Usare questa opzione quando è necessario usare una specifica versione di segreto.</span><span class="sxs-lookup"><span data-stu-id="81d89-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="81d89-126">-Name</span><span class="sxs-lookup"><span data-stu-id="81d89-126">-Name</span></span>
<span data-ttu-id="81d89-127">Specifica il nome del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d89-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="81d89-128">-Password</span><span class="sxs-lookup"><span data-stu-id="81d89-128">-Password</span></span>
<span data-ttu-id="81d89-129">Specifica la password del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d89-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="81d89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d89-130">CommonParameters</span></span>
<span data-ttu-id="81d89-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d89-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d89-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d89-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="81d89-133">INPUTS</span></span>

### <span data-ttu-id="81d89-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81d89-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81d89-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81d89-135">OUTPUTS</span></span>

### <span data-ttu-id="81d89-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81d89-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81d89-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="81d89-137">NOTES</span></span>

## <span data-ttu-id="81d89-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81d89-138">RELATED LINKS</span></span>

[<span data-ttu-id="81d89-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81d89-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="81d89-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81d89-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="81d89-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81d89-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="81d89-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="81d89-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


