---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476208"
---
# <span data-ttu-id="e88eb-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="e88eb-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="e88eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e88eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e88eb-103">Esporta i dati del dominio di sicurezza di un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="e88eb-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="e88eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e88eb-104">SYNTAX</span></span>

### <span data-ttu-id="e88eb-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e88eb-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e88eb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e88eb-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88eb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e88eb-107">DESCRIPTION</span></span>
<span data-ttu-id="e88eb-108">Esporta i dati del dominio di sicurezza di un HSM gestito per l'importazione in un altro HSM.</span><span class="sxs-lookup"><span data-stu-id="e88eb-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="e88eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e88eb-109">EXAMPLES</span></span>

### <span data-ttu-id="e88eb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e88eb-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="e88eb-111">Questo comando Recupera l'HSM gestito denominato testmhsm e salva una copia di backup del dominio di sicurezza di HSM gestito nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="e88eb-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="e88eb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e88eb-112">PARAMETERS</span></span>

### <span data-ttu-id="e88eb-113">-Certificati</span><span class="sxs-lookup"><span data-stu-id="e88eb-113">-Certificates</span></span>
<span data-ttu-id="e88eb-114">Percorsi per i certificati usati per crittografare i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e88eb-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="e88eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88eb-115">-DefaultProfile</span></span>
<span data-ttu-id="e88eb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e88eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88eb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e88eb-117">-Force</span></span>
<span data-ttu-id="e88eb-118">Specificare se sovrascrivere il file esistente.</span><span class="sxs-lookup"><span data-stu-id="e88eb-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="e88eb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e88eb-119">-InputObject</span></span>
<span data-ttu-id="e88eb-120">Oggetto che rappresenta un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="e88eb-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="e88eb-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e88eb-121">-Name</span></span>
<span data-ttu-id="e88eb-122">Nome dell'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="e88eb-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="e88eb-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e88eb-123">-OutputPath</span></span>
<span data-ttu-id="e88eb-124">Specificare il percorso in cui verranno scaricati i dati del dominio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e88eb-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="e88eb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e88eb-125">-PassThru</span></span>
<span data-ttu-id="e88eb-126">Se specificato, viene restituito un valore booleano quando il cmdlet riesce.</span><span class="sxs-lookup"><span data-stu-id="e88eb-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="e88eb-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="e88eb-127">-Quorum</span></span>
<span data-ttu-id="e88eb-128">Numero minimo di condivisioni necessarie per decrittografare il dominio di sicurezza per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="e88eb-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="e88eb-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e88eb-129">-Confirm</span></span>
<span data-ttu-id="e88eb-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e88eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88eb-131">-WhatIf</span></span>
<span data-ttu-id="e88eb-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e88eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88eb-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e88eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88eb-134">CommonParameters</span></span>
<span data-ttu-id="e88eb-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88eb-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e88eb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88eb-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e88eb-137">INPUTS</span></span>

### <span data-ttu-id="e88eb-138">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e88eb-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="e88eb-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e88eb-139">OUTPUTS</span></span>

### <span data-ttu-id="e88eb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e88eb-140">System.Boolean</span></span>

## <span data-ttu-id="e88eb-141">Note</span><span class="sxs-lookup"><span data-stu-id="e88eb-141">NOTES</span></span>

## <span data-ttu-id="e88eb-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e88eb-142">RELATED LINKS</span></span>
