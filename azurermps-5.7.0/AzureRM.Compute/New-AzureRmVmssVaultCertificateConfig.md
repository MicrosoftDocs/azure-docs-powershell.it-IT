---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 9014c91626d41e66f316b870e042af7d5655f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518187"
---
# <span data-ttu-id="3d2a8-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="3d2a8-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="3d2a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2a8-103">Crea una configurazione chiave del certificato Vault.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d2a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d2a8-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d2a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d2a8-105">DESCRIPTION</span></span>
<span data-ttu-id="3d2a8-106">Il cmdlet **New-AzureRmVmssVaultCertificateConfig** specifica il segreto che deve essere inserito nelle macchine virtuali vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="3d2a8-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="3d2a8-107">L'output di questo cmdlet è destinato a essere usato con il cmdlet Add-AzureRmVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="3d2a8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d2a8-108">EXAMPLES</span></span>

### <span data-ttu-id="3d2a8-109">Esempio 1: creare una configurazione chiave del certificato Vault</span><span class="sxs-lookup"><span data-stu-id="3d2a8-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="3d2a8-110">Questo comando crea una configurazione chiave del certificato Vault che usa l'archivio certificati denominato certs situato nell'URL del certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="3d2a8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d2a8-111">PARAMETERS</span></span>

### <span data-ttu-id="3d2a8-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="3d2a8-112">-CertificateStore</span></span>
<span data-ttu-id="3d2a8-113">Specifica l'archivio certificati nelle macchine virtuali nel set di proporzioni in cui viene aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="3d2a8-114">Questa operazione è valida solo per i set di scale della macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d2a8-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="3d2a8-115">-CertificateUrl</span></span>
<span data-ttu-id="3d2a8-116">Specifica l'URI di un certificato archiviato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="3d2a8-117">Si tratta della codifica Base64 dell'oggetto JSON seguente codificato in UTF-8:</span><span class="sxs-lookup"><span data-stu-id="3d2a8-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="3d2a8-118">{"data": " \<Base64-encoded-certificate\> ", "tipo di dati": "pfx", "password": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="3d2a8-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d2a8-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3d2a8-119">-Confirm</span></span>
<span data-ttu-id="3d2a8-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d2a8-121">-WhatIf</span></span>
<span data-ttu-id="3d2a8-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d2a8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2a8-124">CommonParameters</span></span>
<span data-ttu-id="3d2a8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2a8-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d2a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2a8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d2a8-127">INPUTS</span></span>

### <span data-ttu-id="3d2a8-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3d2a8-128">None</span></span>
<span data-ttu-id="3d2a8-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d2a8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d2a8-130">OUTPUTS</span></span>

###  
<span data-ttu-id="3d2a8-131">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3d2a8-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3d2a8-132">Note</span><span class="sxs-lookup"><span data-stu-id="3d2a8-132">NOTES</span></span>

## <span data-ttu-id="3d2a8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d2a8-133">RELATED LINKS</span></span>

[<span data-ttu-id="3d2a8-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="3d2a8-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)