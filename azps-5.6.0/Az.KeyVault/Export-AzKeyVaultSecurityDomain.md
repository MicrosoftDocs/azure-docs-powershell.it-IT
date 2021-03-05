---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 6373ddf37e95c8451afbe8a24b6bade2ca5d3bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994222"
---
# <span data-ttu-id="af677-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="af677-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="af677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af677-102">SYNOPSIS</span></span>
<span data-ttu-id="af677-103">Esporta i dati del dominio di sicurezza di un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="af677-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="af677-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af677-104">SYNTAX</span></span>

### <span data-ttu-id="af677-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af677-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af677-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af677-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af677-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="af677-107">DESCRIPTION</span></span>
<span data-ttu-id="af677-108">Esporta i dati del dominio di sicurezza di un servizio HSM gestito per l'importazione in un altro servizio HSM.</span><span class="sxs-lookup"><span data-stu-id="af677-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="af677-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af677-109">EXAMPLES</span></span>

### <span data-ttu-id="af677-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af677-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="af677-111">Questo comando recupera il file HSM denominato testmhsm gestito e salva una copia di backup del dominio di sicurezza HSM gestito nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="af677-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="af677-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af677-112">PARAMETERS</span></span>

### <span data-ttu-id="af677-113">-Certificates</span><span class="sxs-lookup"><span data-stu-id="af677-113">-Certificates</span></span>
<span data-ttu-id="af677-114">Percorsi dei certificati usati per crittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="af677-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af677-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af677-115">-DefaultProfile</span></span>
<span data-ttu-id="af677-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af677-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af677-117">-Force</span><span class="sxs-lookup"><span data-stu-id="af677-117">-Force</span></span>
<span data-ttu-id="af677-118">Specificare se sovrascrivere il file esistente.</span><span class="sxs-lookup"><span data-stu-id="af677-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="af677-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af677-119">-InputObject</span></span>
<span data-ttu-id="af677-120">Oggetto che rappresenta un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="af677-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="af677-121">-Name</span><span class="sxs-lookup"><span data-stu-id="af677-121">-Name</span></span>
<span data-ttu-id="af677-122">Nome del servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="af677-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="af677-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="af677-123">-OutputPath</span></span>
<span data-ttu-id="af677-124">Specificare il percorso in cui verranno scaricati i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="af677-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="af677-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af677-125">-PassThru</span></span>
<span data-ttu-id="af677-126">Se specificato, verrà restituita una booleana quando il cmdlet ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="af677-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="af677-127">-São</span><span class="sxs-lookup"><span data-stu-id="af677-127">-Quorum</span></span>
<span data-ttu-id="af677-128">Il numero minimo di condivisioni necessario per decrittografare il dominio di sicurezza per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="af677-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af677-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af677-129">-Confirm</span></span>
<span data-ttu-id="af677-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af677-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af677-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af677-131">-WhatIf</span></span>
<span data-ttu-id="af677-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af677-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af677-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af677-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af677-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af677-134">CommonParameters</span></span>
<span data-ttu-id="af677-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af677-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af677-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af677-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af677-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="af677-137">INPUTS</span></span>

### <span data-ttu-id="af677-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="af677-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="af677-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af677-139">OUTPUTS</span></span>

### <span data-ttu-id="af677-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af677-140">System.Boolean</span></span>

## <span data-ttu-id="af677-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="af677-141">NOTES</span></span>

## <span data-ttu-id="af677-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af677-142">RELATED LINKS</span></span>
