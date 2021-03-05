---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 2567d43220193e9233322fbf8715f7b7698890b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983277"
---
# <span data-ttu-id="c19e1-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c19e1-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="c19e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c19e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c19e1-103">Aggiorna un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="c19e1-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="c19e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c19e1-104">SYNTAX</span></span>

### <span data-ttu-id="c19e1-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="c19e1-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19e1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c19e1-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c19e1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c19e1-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c19e1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c19e1-108">DESCRIPTION</span></span>
<span data-ttu-id="c19e1-109">Aggiorna un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="c19e1-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="c19e1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c19e1-110">EXAMPLES</span></span>

### <span data-ttu-id="c19e1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c19e1-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="c19e1-112">Aggiorna il set di crittografia del disco usando la chiave attiva specificata nel vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="c19e1-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="c19e1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c19e1-113">PARAMETERS</span></span>

### <span data-ttu-id="c19e1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c19e1-114">-AsJob</span></span>
<span data-ttu-id="c19e1-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c19e1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c19e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19e1-116">-DefaultProfile</span></span>
<span data-ttu-id="c19e1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c19e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c19e1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c19e1-118">-InputObject</span></span>
<span data-ttu-id="c19e1-119">Oggetto locale del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="c19e1-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c19e1-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="c19e1-120">-KeyUrl</span></span>
<span data-ttu-id="c19e1-121">URL che punta alla chiave attiva in KeyVault</span><span class="sxs-lookup"><span data-stu-id="c19e1-121">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19e1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c19e1-122">-Name</span></span>
<span data-ttu-id="c19e1-123">Nome del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="c19e1-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="c19e1-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c19e1-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19e1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c19e1-126">-ResourceId</span></span>
<span data-ttu-id="c19e1-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c19e1-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19e1-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="c19e1-128">-SourceVaultId</span></span>
<span data-ttu-id="c19e1-129">ID risorsa della chiaveVault contenente la chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="c19e1-129">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19e1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="c19e1-130">-Tag</span></span>
<span data-ttu-id="c19e1-131">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c19e1-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c19e1-132">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c19e1-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c19e1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c19e1-133">-Confirm</span></span>
<span data-ttu-id="c19e1-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c19e1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19e1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19e1-135">-WhatIf</span></span>
<span data-ttu-id="c19e1-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c19e1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19e1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c19e1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19e1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19e1-138">CommonParameters</span></span>
<span data-ttu-id="c19e1-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19e1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19e1-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c19e1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19e1-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="c19e1-141">INPUTS</span></span>

### <span data-ttu-id="c19e1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c19e1-142">System.String</span></span>

### <span data-ttu-id="c19e1-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c19e1-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="c19e1-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c19e1-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c19e1-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c19e1-145">OUTPUTS</span></span>

### <span data-ttu-id="c19e1-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c19e1-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="c19e1-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="c19e1-147">NOTES</span></span>

## <span data-ttu-id="c19e1-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c19e1-148">RELATED LINKS</span></span>
