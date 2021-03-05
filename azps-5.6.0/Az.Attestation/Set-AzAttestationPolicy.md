---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c32a9e2fd474578c8526c8352e8649cb84d8b016
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966782"
---
# <span data-ttu-id="86a71-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="86a71-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="86a71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86a71-102">SYNOPSIS</span></span>
<span data-ttu-id="86a71-103">Imposta il criterio da un tenant in Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="86a71-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="86a71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86a71-104">SYNTAX</span></span>

### <span data-ttu-id="86a71-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86a71-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86a71-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86a71-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86a71-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86a71-107">DESCRIPTION</span></span>
<span data-ttu-id="86a71-108">Il Set-AzAttestationPolicy cmdlet imposta il criterio da un tenant in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="86a71-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="86a71-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86a71-109">EXAMPLES</span></span>

### <span data-ttu-id="86a71-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86a71-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="86a71-111">Imposta i criteri definiti dall'utente per il tipo di TEE *SgxEnclave* per Attestation Provider *pshtest* usando un formato di criteri di testo (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="86a71-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="86a71-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="86a71-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="86a71-113">Imposta i criteri definiti dall'utente per il tipo di TEE *SgxEnclave* per Attestation Provider *pshtest* usando un formato di criteri JWT.</span><span class="sxs-lookup"><span data-stu-id="86a71-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="86a71-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86a71-114">PARAMETERS</span></span>

### <span data-ttu-id="86a71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a71-115">-DefaultProfile</span></span>
<span data-ttu-id="86a71-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86a71-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86a71-117">-Name</span><span class="sxs-lookup"><span data-stu-id="86a71-117">-Name</span></span>
<span data-ttu-id="86a71-118">Specifica un nome del tenant.</span><span class="sxs-lookup"><span data-stu-id="86a71-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="86a71-119">Questo cmdlet imposta i criteri di attestazione per il tenant specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="86a71-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86a71-120">-PassThru</span></span>
<span data-ttu-id="86a71-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="86a71-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="86a71-122">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="86a71-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="86a71-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="86a71-123">-Policy</span></span>
<span data-ttu-id="86a71-124">Specifica il documento dei criteri da impostare.</span><span class="sxs-lookup"><span data-stu-id="86a71-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="86a71-125">Il formato dei criteri può essere Testo o Token Web JSON (JWT).</span><span class="sxs-lookup"><span data-stu-id="86a71-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="86a71-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="86a71-126">-PolicyFormat</span></span>
<span data-ttu-id="86a71-127">Specifica il formato del criterio, testo o JWT (token Web JSON).</span><span class="sxs-lookup"><span data-stu-id="86a71-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="86a71-128">Il formato predefinito dei criteri è Testo.</span><span class="sxs-lookup"><span data-stu-id="86a71-128">The default policy format is Text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a71-129">-ResourceGroupName</span></span>
<span data-ttu-id="86a71-130">Specifica il nome del gruppo di risorse di un provider di attestazione.</span><span class="sxs-lookup"><span data-stu-id="86a71-130">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86a71-131">-ResourceId</span></span>
<span data-ttu-id="86a71-132">Specifica l'ID Risorsa di un provider di attestazioni.</span><span class="sxs-lookup"><span data-stu-id="86a71-132">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="86a71-133">-Tee</span></span>
<span data-ttu-id="86a71-134">Specifica un tipo di ambiente di esecuzione attendibile.</span><span class="sxs-lookup"><span data-stu-id="86a71-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="86a71-135">Sono supportati quattro tipi di ambiente: SgxEnclave, OpenEnclave, CyRes Piattaforme e VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="86a71-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="86a71-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86a71-136">-Confirm</span></span>
<span data-ttu-id="86a71-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86a71-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86a71-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86a71-138">-WhatIf</span></span>
<span data-ttu-id="86a71-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86a71-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86a71-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86a71-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86a71-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a71-141">CommonParameters</span></span>
<span data-ttu-id="86a71-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a71-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a71-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86a71-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a71-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="86a71-144">INPUTS</span></span>

### <span data-ttu-id="86a71-145">System.String</span><span class="sxs-lookup"><span data-stu-id="86a71-145">System.String</span></span>

## <span data-ttu-id="86a71-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86a71-146">OUTPUTS</span></span>

### <span data-ttu-id="86a71-147">System.String</span><span class="sxs-lookup"><span data-stu-id="86a71-147">System.String</span></span>

## <span data-ttu-id="86a71-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="86a71-148">NOTES</span></span>

## <span data-ttu-id="86a71-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86a71-149">RELATED LINKS</span></span>
