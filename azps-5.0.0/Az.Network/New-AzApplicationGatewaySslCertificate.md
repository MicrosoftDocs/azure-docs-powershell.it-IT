---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: a5a1533038f8e11a30dd3fdeedd590b8186597b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310260"
---
# <span data-ttu-id="264a4-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="264a4-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="264a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="264a4-102">SYNOPSIS</span></span>
<span data-ttu-id="264a4-103">Crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="264a4-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="264a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="264a4-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="264a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="264a4-105">DESCRIPTION</span></span>
<span data-ttu-id="264a4-106">Il cmdlet **New-AzApplicationGatewaySslCertificate** crea un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="264a4-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="264a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="264a4-107">EXAMPLES</span></span>

### <span data-ttu-id="264a4-108">Esempio 1: creare un certificato SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="264a4-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="264a4-109">Questo comando crea un certificato SSL denominato Cert01 per il gateway applicazione predefinito e archivia il risultato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="264a4-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="264a4-110">Esempio 2: creare un certificato SSL usando il segreto di Vault (versione meno secretId) e aggiungerlo a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="264a4-111">Ottenere il segreto e creare un certificato SSL in uso `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="264a4-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="264a4-112">Nota: la versione meno secretId è disponibile qui, Application Gateway sincronizza il certificato in intervalli regolari con il Vault.</span><span class="sxs-lookup"><span data-stu-id="264a4-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="264a4-113">Esempio 3: creare un certificato SSL usando il segreto di Vault e aggiungerlo a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="264a4-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="264a4-114">Ottenere il segreto e creare un certificato SSL in uso `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="264a4-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="264a4-115">Nota: se è necessario che il gateway dell'applicazione sincronizza il certificato con il Vault, fornisci la versione meno secretId.</span><span class="sxs-lookup"><span data-stu-id="264a4-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="264a4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="264a4-116">PARAMETERS</span></span>

### <span data-ttu-id="264a4-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="264a4-117">-CertificateFile</span></span>
<span data-ttu-id="264a4-118">Specifica il percorso del file pfx del certificato SSL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="264a4-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="264a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="264a4-119">-DefaultProfile</span></span>
<span data-ttu-id="264a4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="264a4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="264a4-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="264a4-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="264a4-122">SecretId (URI) del segreto del Vault.</span><span class="sxs-lookup"><span data-stu-id="264a4-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="264a4-123">Usa questa opzione quando è necessario usare una specifica versione di segreto.</span><span class="sxs-lookup"><span data-stu-id="264a4-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="264a4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="264a4-124">-Name</span></span>
<span data-ttu-id="264a4-125">Specifica il nome del certificato SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="264a4-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="264a4-126">-Password</span><span class="sxs-lookup"><span data-stu-id="264a4-126">-Password</span></span>
<span data-ttu-id="264a4-127">Specifica la password del protocollo SSL creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="264a4-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="264a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264a4-128">CommonParameters</span></span>
<span data-ttu-id="264a4-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="264a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264a4-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="264a4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264a4-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="264a4-131">INPUTS</span></span>

### <span data-ttu-id="264a4-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="264a4-132">None</span></span>

## <span data-ttu-id="264a4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="264a4-133">OUTPUTS</span></span>

### <span data-ttu-id="264a4-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="264a4-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="264a4-135">Note</span><span class="sxs-lookup"><span data-stu-id="264a4-135">NOTES</span></span>

## <span data-ttu-id="264a4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="264a4-136">RELATED LINKS</span></span>

[<span data-ttu-id="264a4-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="264a4-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="264a4-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="264a4-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="264a4-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="264a4-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="264a4-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="264a4-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


