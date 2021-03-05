---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 3175685478afada44e8870e772a56ce91992bbc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001405"
---
# <span data-ttu-id="73cfc-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="73cfc-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="73cfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="73cfc-103">Importa i dati del dominio di sicurezza esportati in precedenza in un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="73cfc-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="73cfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73cfc-104">SYNTAX</span></span>

### <span data-ttu-id="73cfc-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73cfc-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73cfc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="73cfc-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73cfc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="73cfc-107">DESCRIPTION</span></span>
<span data-ttu-id="73cfc-108">Questo cmdlet importa i dati del dominio di sicurezza esportati in precedenza in un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="73cfc-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="73cfc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73cfc-109">EXAMPLES</span></span>

### <span data-ttu-id="73cfc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73cfc-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="73cfc-111">Prima di tutto, è necessario fornite le chiavi per decrittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="73cfc-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="73cfc-112">Il comando **Import-AzKeyVaultSecurityDomain** ripristina quindi i dati del dominio di sicurezza di cui è stato eseguito il backup precedente in un servizio HSM gestito usando queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="73cfc-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="73cfc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73cfc-113">PARAMETERS</span></span>

### <span data-ttu-id="73cfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cfc-114">-DefaultProfile</span></span>
<span data-ttu-id="73cfc-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73cfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73cfc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73cfc-116">-InputObject</span></span>
<span data-ttu-id="73cfc-117">Oggetto che rappresenta un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="73cfc-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="73cfc-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="73cfc-118">-Keys</span></span>
<span data-ttu-id="73cfc-119">Informazioni sulle chiavi usate per decrittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="73cfc-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="73cfc-120">Vedere esempi su come è costruita.</span><span class="sxs-lookup"><span data-stu-id="73cfc-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="73cfc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="73cfc-121">-Name</span></span>
<span data-ttu-id="73cfc-122">Nome del servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="73cfc-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="73cfc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73cfc-123">-PassThru</span></span>
<span data-ttu-id="73cfc-124">Se specificato, verrà restituita una booleana quando il cmdlet ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="73cfc-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="73cfc-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="73cfc-125">-SecurityDomainPath</span></span>
<span data-ttu-id="73cfc-126">Specificare il percorso dei dati del dominio di sicurezza crittografato.</span><span class="sxs-lookup"><span data-stu-id="73cfc-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="73cfc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73cfc-127">-Confirm</span></span>
<span data-ttu-id="73cfc-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73cfc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73cfc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73cfc-129">-WhatIf</span></span>
<span data-ttu-id="73cfc-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73cfc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73cfc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73cfc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73cfc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cfc-132">CommonParameters</span></span>
<span data-ttu-id="73cfc-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cfc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cfc-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="73cfc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cfc-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="73cfc-135">INPUTS</span></span>

### <span data-ttu-id="73cfc-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="73cfc-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="73cfc-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73cfc-137">OUTPUTS</span></span>

### <span data-ttu-id="73cfc-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73cfc-138">System.Boolean</span></span>

## <span data-ttu-id="73cfc-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="73cfc-139">NOTES</span></span>

## <span data-ttu-id="73cfc-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73cfc-140">RELATED LINKS</span></span>
