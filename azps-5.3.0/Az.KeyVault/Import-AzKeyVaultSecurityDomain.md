---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476189"
---
# <span data-ttu-id="8ef72-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="8ef72-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="8ef72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ef72-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef72-103">Importa i dati del dominio di sicurezza esportati in precedenza in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="8ef72-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="8ef72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ef72-104">SYNTAX</span></span>

### <span data-ttu-id="8ef72-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ef72-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ef72-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ef72-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ef72-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ef72-107">DESCRIPTION</span></span>
<span data-ttu-id="8ef72-108">Questo cmdlet importa i dati del dominio di sicurezza esportati in precedenza in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="8ef72-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="8ef72-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ef72-109">EXAMPLES</span></span>

### <span data-ttu-id="8ef72-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ef72-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="8ef72-111">Prima di tutto, è necessario fornire le chiavi per decrittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8ef72-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="8ef72-112">Quindi, il comando **Import-AzKeyVaultSecurityDomain** Ripristina i dati del dominio di sicurezza di backup precedenti in un HSM gestito usando questi tasti.</span><span class="sxs-lookup"><span data-stu-id="8ef72-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="8ef72-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ef72-113">PARAMETERS</span></span>

### <span data-ttu-id="8ef72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef72-114">-DefaultProfile</span></span>
<span data-ttu-id="8ef72-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ef72-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ef72-116">-InputObject</span></span>
<span data-ttu-id="8ef72-117">Oggetto che rappresenta un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="8ef72-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="8ef72-118">-Tasti</span><span class="sxs-lookup"><span data-stu-id="8ef72-118">-Keys</span></span>
<span data-ttu-id="8ef72-119">Informazioni sulle chiavi usate per decrittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8ef72-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="8ef72-120">Vedere esempi per il modo in cui viene costruito.</span><span class="sxs-lookup"><span data-stu-id="8ef72-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="8ef72-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ef72-121">-Name</span></span>
<span data-ttu-id="8ef72-122">Nome dell'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="8ef72-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="8ef72-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ef72-123">-PassThru</span></span>
<span data-ttu-id="8ef72-124">Se specificato, viene restituito un valore booleano quando il cmdlet riesce.</span><span class="sxs-lookup"><span data-stu-id="8ef72-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="8ef72-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="8ef72-125">-SecurityDomainPath</span></span>
<span data-ttu-id="8ef72-126">Specificare il percorso per i dati del dominio di sicurezza crittografati.</span><span class="sxs-lookup"><span data-stu-id="8ef72-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="8ef72-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ef72-127">-Confirm</span></span>
<span data-ttu-id="8ef72-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ef72-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ef72-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ef72-129">-WhatIf</span></span>
<span data-ttu-id="8ef72-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ef72-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ef72-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ef72-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ef72-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef72-132">CommonParameters</span></span>
<span data-ttu-id="8ef72-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef72-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef72-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ef72-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef72-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ef72-135">INPUTS</span></span>

### <span data-ttu-id="8ef72-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8ef72-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="8ef72-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ef72-137">OUTPUTS</span></span>

### <span data-ttu-id="8ef72-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ef72-138">System.Boolean</span></span>

## <span data-ttu-id="8ef72-139">Note</span><span class="sxs-lookup"><span data-stu-id="8ef72-139">NOTES</span></span>

## <span data-ttu-id="8ef72-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ef72-140">RELATED LINKS</span></span>
