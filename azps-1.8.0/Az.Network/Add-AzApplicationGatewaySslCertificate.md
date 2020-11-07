---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7dddb6a5b38414d658cc405820327c0d6df43a6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678686"
---
# <span data-ttu-id="3f15f-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f15f-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3f15f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f15f-102">SYNOPSIS</span></span>
<span data-ttu-id="3f15f-103">Aggiunge un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f15f-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="3f15f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f15f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f15f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f15f-105">DESCRIPTION</span></span>
<span data-ttu-id="3f15f-106">Il cmdlet **Add-AzApplicationGatewaySslCertificate** aggiunge un certificato SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f15f-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="3f15f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f15f-107">EXAMPLES</span></span>

### <span data-ttu-id="3f15f-108">Esempio 1: aggiungere un certificato SSL tramite PFX a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f15f-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="3f15f-109">Questo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 e quindi aggiunge un certificato SSL denominato Cert01.</span><span class="sxs-lookup"><span data-stu-id="3f15f-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="3f15f-110">Esempio 2: aggiungere un certificato SSL tramite il segreto di Vault (versione meno secretId) a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f15f-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="3f15f-111">Ottenere il segreto e farvi riferimento in `Add-AzApplicationGatewaySslCertificate` per aggiungerlo al gateway dell'applicazione con nome `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="3f15f-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="3f15f-112">Nota: la versione meno secretId è disponibile qui, Application Gateway sincronizza il certificato in intervalli regolari con il Vault.</span><span class="sxs-lookup"><span data-stu-id="3f15f-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="3f15f-113">Esempio 3: aggiungere un certificato SSL usando il segreto del Vault (versione secretId) a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f15f-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="3f15f-114">Ottenere il segreto e farvi riferimento in `Add-AzApplicationGatewaySslCertificate` per aggiungerlo al gateway dell'applicazione con nome `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="3f15f-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="3f15f-115">Nota: se è necessario che il gateway dell'applicazione sincronizza il certificato con il Vault, fornisci la versione meno secretId.</span><span class="sxs-lookup"><span data-stu-id="3f15f-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="3f15f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f15f-116">PARAMETERS</span></span>

### <span data-ttu-id="3f15f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f15f-117">-ApplicationGateway</span></span>
<span data-ttu-id="3f15f-118">Specifica il nome del gateway dell'applicazione a cui questo cmdlet aggiunge un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="3f15f-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="3f15f-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3f15f-119">-CertificateFile</span></span>
<span data-ttu-id="3f15f-120">Specifica il file PFX di un certificato SSL aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f15f-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3f15f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f15f-121">-DefaultProfile</span></span>
<span data-ttu-id="3f15f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f15f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f15f-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="3f15f-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="3f15f-124">SecretId (URI) del segreto del Vault.</span><span class="sxs-lookup"><span data-stu-id="3f15f-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="3f15f-125">Usa questa opzione quando è necessario usare una specifica versione di segreto.</span><span class="sxs-lookup"><span data-stu-id="3f15f-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="3f15f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f15f-126">-Name</span></span>
<span data-ttu-id="3f15f-127">Specifica il nome del certificato SSL aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f15f-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3f15f-128">-Password</span><span class="sxs-lookup"><span data-stu-id="3f15f-128">-Password</span></span>
<span data-ttu-id="3f15f-129">Specifica la password del certificato SSL aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f15f-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3f15f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f15f-130">CommonParameters</span></span>
<span data-ttu-id="3f15f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f15f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f15f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f15f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f15f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f15f-133">INPUTS</span></span>

### <span data-ttu-id="3f15f-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f15f-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f15f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f15f-135">OUTPUTS</span></span>

### <span data-ttu-id="3f15f-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f15f-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f15f-137">Note</span><span class="sxs-lookup"><span data-stu-id="3f15f-137">NOTES</span></span>

## <span data-ttu-id="3f15f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f15f-138">RELATED LINKS</span></span>

[<span data-ttu-id="3f15f-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f15f-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3f15f-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f15f-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3f15f-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f15f-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3f15f-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f15f-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


