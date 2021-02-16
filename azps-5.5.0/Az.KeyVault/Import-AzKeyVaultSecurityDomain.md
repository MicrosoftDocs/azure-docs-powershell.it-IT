---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209306"
---
# <span data-ttu-id="eabbe-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="eabbe-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="eabbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eabbe-102">SYNOPSIS</span></span>
<span data-ttu-id="eabbe-103">Importa i dati del dominio di sicurezza esportati in precedenza in un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="eabbe-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="eabbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eabbe-104">SYNTAX</span></span>

### <span data-ttu-id="eabbe-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eabbe-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eabbe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eabbe-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eabbe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eabbe-107">DESCRIPTION</span></span>
<span data-ttu-id="eabbe-108">Questo cmdlet importa i dati del dominio di sicurezza esportati in precedenza in un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="eabbe-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="eabbe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eabbe-109">EXAMPLES</span></span>

### <span data-ttu-id="eabbe-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eabbe-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="eabbe-111">Prima di tutto, è necessario fornite le chiavi per decrittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="eabbe-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="eabbe-112">Il comando **Import-AzKeyVaultSecurityDomain** ripristina quindi i dati del dominio di sicurezza di cui è stato eseguito il backup precedente in un servizio HSM gestito usando queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="eabbe-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="eabbe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eabbe-113">PARAMETERS</span></span>

### <span data-ttu-id="eabbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabbe-114">-DefaultProfile</span></span>
<span data-ttu-id="eabbe-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eabbe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eabbe-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eabbe-116">-InputObject</span></span>
<span data-ttu-id="eabbe-117">Oggetto che rappresenta un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="eabbe-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eabbe-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="eabbe-118">-Keys</span></span>
<span data-ttu-id="eabbe-119">Informazioni sulle chiavi usate per decrittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="eabbe-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="eabbe-120">Vedere esempi su come è costruita.</span><span class="sxs-lookup"><span data-stu-id="eabbe-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabbe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eabbe-121">-Name</span></span>
<span data-ttu-id="eabbe-122">Nome del servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="eabbe-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabbe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eabbe-123">-PassThru</span></span>
<span data-ttu-id="eabbe-124">Se specificato, verrà restituita una booleana quando il cmdlet ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="eabbe-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="eabbe-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="eabbe-125">-SecurityDomainPath</span></span>
<span data-ttu-id="eabbe-126">Specificare il percorso dei dati del dominio di sicurezza crittografato.</span><span class="sxs-lookup"><span data-stu-id="eabbe-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eabbe-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eabbe-127">-Confirm</span></span>
<span data-ttu-id="eabbe-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eabbe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eabbe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eabbe-129">-WhatIf</span></span>
<span data-ttu-id="eabbe-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eabbe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eabbe-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eabbe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eabbe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabbe-132">CommonParameters</span></span>
<span data-ttu-id="eabbe-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabbe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabbe-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eabbe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabbe-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="eabbe-135">INPUTS</span></span>

### <span data-ttu-id="eabbe-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="eabbe-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="eabbe-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eabbe-137">OUTPUTS</span></span>

### <span data-ttu-id="eabbe-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eabbe-138">System.Boolean</span></span>

## <span data-ttu-id="eabbe-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="eabbe-139">NOTES</span></span>

## <span data-ttu-id="eabbe-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eabbe-140">RELATED LINKS</span></span>
