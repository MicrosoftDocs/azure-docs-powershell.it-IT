---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/stop-azkeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Stop-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: d6def0badcc9973f62beb65dadbb15a39c34e7ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674101"
---
# <span data-ttu-id="2aa28-101">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2aa28-101">Stop-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="2aa28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2aa28-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa28-103">Annulla un'operazione di certificato in Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="2aa28-103">Cancels a certificate operation in key vault.</span></span>

## <span data-ttu-id="2aa28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2aa28-104">SYNTAX</span></span>

### <span data-ttu-id="2aa28-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2aa28-105">Default (Default)</span></span>
```
Stop-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa28-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa28-106">InputObject</span></span>
```
Stop-AzKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa28-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aa28-107">DESCRIPTION</span></span>
<span data-ttu-id="2aa28-108">Il cmdlet **Stop-AzKeyVaultCertificateOperation** Annulla un'operazione di certificato nel servizio di archiviazione delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa28-108">The **Stop-AzKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="2aa28-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2aa28-109">EXAMPLES</span></span>

### <span data-ttu-id="2aa28-110">Esempio 1: annullamento di un'operazione su un certificato</span><span class="sxs-lookup"><span data-stu-id="2aa28-110">Example 1: Cancel a certificate operation</span></span>
```powershell
PS C:\> Stop-AzKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force

Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="2aa28-111">Questo comando Annulla l'operazione del certificato TestCert02.</span><span class="sxs-lookup"><span data-stu-id="2aa28-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="2aa28-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2aa28-112">PARAMETERS</span></span>

### <span data-ttu-id="2aa28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa28-113">-DefaultProfile</span></span>
<span data-ttu-id="2aa28-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2aa28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aa28-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2aa28-115">-Force</span></span>
<span data-ttu-id="2aa28-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2aa28-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa28-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa28-117">-InputObject</span></span>
<span data-ttu-id="2aa28-118">Oggetto Operation</span><span class="sxs-lookup"><span data-stu-id="2aa28-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa28-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2aa28-119">-Name</span></span>
<span data-ttu-id="2aa28-120">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="2aa28-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa28-121">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="2aa28-121">-VaultName</span></span>
<span data-ttu-id="2aa28-122">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="2aa28-122">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa28-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2aa28-123">-Confirm</span></span>
<span data-ttu-id="2aa28-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aa28-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa28-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa28-125">-WhatIf</span></span>
<span data-ttu-id="2aa28-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aa28-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa28-127">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aa28-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa28-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aa28-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa28-129">CommonParameters</span></span>
<span data-ttu-id="2aa28-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa28-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa28-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa28-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2aa28-132">INPUTS</span></span>

### <span data-ttu-id="2aa28-133">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2aa28-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="2aa28-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2aa28-134">OUTPUTS</span></span>

### <span data-ttu-id="2aa28-135">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2aa28-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="2aa28-136">Note</span><span class="sxs-lookup"><span data-stu-id="2aa28-136">NOTES</span></span>

## <span data-ttu-id="2aa28-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2aa28-137">RELATED LINKS</span></span>

[<span data-ttu-id="2aa28-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2aa28-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="2aa28-139">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="2aa28-139">Remove-AzKeyVaultCertificateOperation</span></span>](./Remove-AzKeyVaultCertificateOperation.md)

