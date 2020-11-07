---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 0afd599bd1af9b3f597e9753d1be1e8ae710e5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675300"
---
# <span data-ttu-id="148e4-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="148e4-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="148e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="148e4-102">SYNOPSIS</span></span>
<span data-ttu-id="148e4-103">Crea una configurazione chiave del certificato Vault.</span><span class="sxs-lookup"><span data-stu-id="148e4-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="148e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="148e4-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="148e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="148e4-105">DESCRIPTION</span></span>
<span data-ttu-id="148e4-106">Il cmdlet **New-AzVmssVaultCertificateConfig** specifica il segreto che deve essere inserito nelle macchine virtuali vmss (Virtual Machine scale set).</span><span class="sxs-lookup"><span data-stu-id="148e4-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="148e4-107">L'output di questo cmdlet è destinato a essere usato con il cmdlet Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="148e4-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="148e4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="148e4-108">EXAMPLES</span></span>

### <span data-ttu-id="148e4-109">Esempio 1: creare una configurazione chiave del certificato Vault</span><span class="sxs-lookup"><span data-stu-id="148e4-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="148e4-110">Questo comando crea una configurazione chiave del certificato Vault che usa l'archivio certificati denominato certs situato nell'URL del certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="148e4-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="148e4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="148e4-111">PARAMETERS</span></span>

### <span data-ttu-id="148e4-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="148e4-112">-CertificateStore</span></span>
<span data-ttu-id="148e4-113">Specifica l'archivio certificati nelle macchine virtuali nel set di proporzioni in cui viene aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="148e4-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="148e4-114">Questa operazione è valida solo per i set di scale della macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="148e4-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="148e4-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="148e4-115">-CertificateUrl</span></span>
<span data-ttu-id="148e4-116">Specifica l'URI di un certificato archiviato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="148e4-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="148e4-117">Si tratta della codifica Base64 dell'oggetto JSON seguente codificato in UTF-8: {"data": "codifica \< base64-certificato \> ", "DataType": "pfx", "password": " \< pfx-file-password \> "}</span><span class="sxs-lookup"><span data-stu-id="148e4-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="148e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148e4-118">-DefaultProfile</span></span>
<span data-ttu-id="148e4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="148e4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="148e4-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="148e4-120">-Confirm</span></span>
<span data-ttu-id="148e4-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="148e4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="148e4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="148e4-122">-WhatIf</span></span>
<span data-ttu-id="148e4-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="148e4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="148e4-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="148e4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="148e4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148e4-125">CommonParameters</span></span>
<span data-ttu-id="148e4-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="148e4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148e4-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="148e4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148e4-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="148e4-128">INPUTS</span></span>

### <span data-ttu-id="148e4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="148e4-129">System.String</span></span>

## <span data-ttu-id="148e4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="148e4-130">OUTPUTS</span></span>

### <span data-ttu-id="148e4-131">Microsoft. Azure. Management. Compute. Models. VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="148e4-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="148e4-132">Note</span><span class="sxs-lookup"><span data-stu-id="148e4-132">NOTES</span></span>

## <span data-ttu-id="148e4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="148e4-133">RELATED LINKS</span></span>

[<span data-ttu-id="148e4-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="148e4-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
