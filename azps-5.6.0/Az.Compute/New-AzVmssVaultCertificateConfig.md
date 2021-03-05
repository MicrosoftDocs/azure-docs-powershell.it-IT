---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: cc607e12873e0b5b738a64d781d16ed73bc72f7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988398"
---
# <span data-ttu-id="2feb7-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="2feb7-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="2feb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2feb7-102">SYNOPSIS</span></span>
<span data-ttu-id="2feb7-103">Crea una configurazione del certificato del Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="2feb7-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="2feb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2feb7-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2feb7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2feb7-105">DESCRIPTION</span></span>
<span data-ttu-id="2feb7-106">Il cmdlet **New-AzVmssVaultCertificateConfig** specifica il segreto che deve essere inserito nelle macchine virtuali VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="2feb7-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="2feb7-107">L'output di questo cmdlet è destinato a essere usato con il cmdlet Add-AzVmssSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2feb7-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="2feb7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2feb7-108">EXAMPLES</span></span>

### <span data-ttu-id="2feb7-109">Esempio 1: Creare una configurazione del certificato del Vault chiave</span><span class="sxs-lookup"><span data-stu-id="2feb7-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="2feb7-110">Questo comando crea una configurazione del certificato del Vault delle chiavi che usa l'archivio certificati denominato MyCerts situato all'URL del certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="2feb7-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="2feb7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2feb7-111">PARAMETERS</span></span>

### <span data-ttu-id="2feb7-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="2feb7-112">-CertificateStore</span></span>
<span data-ttu-id="2feb7-113">Specifica l'archivio certificati nelle macchine virtuali nel set di scala in cui viene aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="2feb7-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="2feb7-114">Questo valore è valido solo per i set di scalabilità delle macchine virtuali di Windows.</span><span class="sxs-lookup"><span data-stu-id="2feb7-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

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

### <span data-ttu-id="2feb7-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="2feb7-115">-CertificateUrl</span></span>
<span data-ttu-id="2feb7-116">Specifica l'URI di un certificato archiviato nel Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="2feb7-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="2feb7-117">È la codifica base64 dell'oggetto JSON seguente codificato in UTF-8: { "data":" \<Base64-encoded-certificate\> ", "dataType":"pfx", "password":" \<pfx-file-password\> " }</span><span class="sxs-lookup"><span data-stu-id="2feb7-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

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

### <span data-ttu-id="2feb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2feb7-118">-DefaultProfile</span></span>
<span data-ttu-id="2feb7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2feb7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2feb7-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2feb7-120">-Confirm</span></span>
<span data-ttu-id="2feb7-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2feb7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2feb7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2feb7-122">-WhatIf</span></span>
<span data-ttu-id="2feb7-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2feb7-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2feb7-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2feb7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2feb7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2feb7-125">CommonParameters</span></span>
<span data-ttu-id="2feb7-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2feb7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2feb7-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2feb7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2feb7-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="2feb7-128">INPUTS</span></span>

### <span data-ttu-id="2feb7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2feb7-129">System.String</span></span>

## <span data-ttu-id="2feb7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2feb7-130">OUTPUTS</span></span>

### <span data-ttu-id="2feb7-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2feb7-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="2feb7-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="2feb7-132">NOTES</span></span>

## <span data-ttu-id="2feb7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2feb7-133">RELATED LINKS</span></span>

[<span data-ttu-id="2feb7-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="2feb7-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
