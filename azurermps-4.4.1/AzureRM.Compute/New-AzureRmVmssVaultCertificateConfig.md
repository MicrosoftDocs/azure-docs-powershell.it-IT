---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssVaultCertificateConfig.md
ms.openlocfilehash: 5dd9b4f8dded86a0a900a3bb3942b633c29f7020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521266"
---
# <span data-ttu-id="a9858-101">New-AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="a9858-101">New-AzureRmVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="a9858-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9858-102">SYNOPSIS</span></span>
<span data-ttu-id="a9858-103">Crea una configurazione chiave del certificato Vault.</span><span class="sxs-lookup"><span data-stu-id="a9858-103">Creates a Key Vault certificate configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9858-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9858-104">SYNTAX</span></span>

```
New-AzureRmVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9858-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9858-105">DESCRIPTION</span></span>
<span data-ttu-id="a9858-106">Il cmdlet **New-AzureRmVmssVaultCertificateConfig** specifica il segreto che deve essere inserito nelle macchine virtuali vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="a9858-106">The **New-AzureRmVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="a9858-107">L'output di questo cmdlet è destinato a essere usato con il cmdlet Add-AzureRmVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="a9858-107">The output of this cmdlet is intended to be used with the Add-AzureRmVmssSecret cmdlet.</span></span>

## <span data-ttu-id="a9858-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9858-108">EXAMPLES</span></span>

### <span data-ttu-id="a9858-109">Esempio 1: creare una configurazione chiave del certificato Vault</span><span class="sxs-lookup"><span data-stu-id="a9858-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="a9858-110">Questo comando crea una configurazione chiave del certificato Vault che usa l'archivio certificati denominato certs situato nell'URL del certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="a9858-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="a9858-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9858-111">PARAMETERS</span></span>

### <span data-ttu-id="a9858-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="a9858-112">-CertificateStore</span></span>
<span data-ttu-id="a9858-113">Specifica l'archivio certificati nelle macchine virtuali nel set di proporzioni in cui viene aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="a9858-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="a9858-114">Questa operazione è valida solo per i set di scale della macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="a9858-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9858-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="a9858-115">-CertificateUrl</span></span>
<span data-ttu-id="a9858-116">Specifica l'URI di un certificato archiviato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="a9858-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>

<span data-ttu-id="a9858-117">Si tratta della codifica Base64 dell'oggetto JSON seguente codificato in UTF-8:</span><span class="sxs-lookup"><span data-stu-id="a9858-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8:</span></span>


<span data-ttu-id="a9858-118">{"data": " \<Base64-encoded-certificate\> ", "tipo di dati": "pfx", "password": " \<pfx-file-password\> "}</span><span class="sxs-lookup"><span data-stu-id="a9858-118">{ "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9858-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9858-119">-DefaultProfile</span></span>
<span data-ttu-id="a9858-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9858-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9858-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9858-121">-Confirm</span></span>
<span data-ttu-id="a9858-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9858-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9858-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9858-123">-WhatIf</span></span>
<span data-ttu-id="a9858-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9858-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9858-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9858-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9858-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9858-126">CommonParameters</span></span>
<span data-ttu-id="a9858-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9858-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9858-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9858-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9858-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9858-129">INPUTS</span></span>

## <span data-ttu-id="a9858-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9858-130">OUTPUTS</span></span>

###  
<span data-ttu-id="a9858-131">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a9858-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a9858-132">Note</span><span class="sxs-lookup"><span data-stu-id="a9858-132">NOTES</span></span>

## <span data-ttu-id="a9858-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9858-133">RELATED LINKS</span></span>

[<span data-ttu-id="a9858-134">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="a9858-134">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)
