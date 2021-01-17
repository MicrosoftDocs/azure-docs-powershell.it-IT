---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473635"
---
# <span data-ttu-id="abf89-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="abf89-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="abf89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abf89-102">SYNOPSIS</span></span>
<span data-ttu-id="abf89-103">Aggiorna un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="abf89-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="abf89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abf89-104">SYNTAX</span></span>

### <span data-ttu-id="abf89-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="abf89-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abf89-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="abf89-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abf89-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="abf89-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abf89-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abf89-108">DESCRIPTION</span></span>
<span data-ttu-id="abf89-109">Aggiorna un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="abf89-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="abf89-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abf89-110">EXAMPLES</span></span>

### <span data-ttu-id="abf89-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="abf89-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="abf89-112">Aggiorna la crittografia del disco impostando la chiave attiva specificata nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="abf89-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="abf89-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abf89-113">PARAMETERS</span></span>

### <span data-ttu-id="abf89-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abf89-114">-AsJob</span></span>
<span data-ttu-id="abf89-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="abf89-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abf89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf89-116">-DefaultProfile</span></span>
<span data-ttu-id="abf89-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abf89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abf89-118">-InputObject</span></span>
<span data-ttu-id="abf89-119">Oggetto local del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="abf89-119">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="abf89-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="abf89-120">-KeyUrl</span></span>
<span data-ttu-id="abf89-121">URL che punta alla chiave attiva in Key Vault</span><span class="sxs-lookup"><span data-stu-id="abf89-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="abf89-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="abf89-122">-Name</span></span>
<span data-ttu-id="abf89-123">Nome del set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="abf89-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="abf89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf89-124">-ResourceGroupName</span></span>
<span data-ttu-id="abf89-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="abf89-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="abf89-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abf89-126">-ResourceId</span></span>
<span data-ttu-id="abf89-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="abf89-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="abf89-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="abf89-128">-SourceVaultId</span></span>
<span data-ttu-id="abf89-129">ID risorsa del caveau contenente il tasto attivo.</span><span class="sxs-lookup"><span data-stu-id="abf89-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="abf89-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="abf89-130">-Tag</span></span>
<span data-ttu-id="abf89-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="abf89-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="abf89-132">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="abf89-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="abf89-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="abf89-133">-Confirm</span></span>
<span data-ttu-id="abf89-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abf89-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf89-135">-WhatIf</span></span>
<span data-ttu-id="abf89-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abf89-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf89-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abf89-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf89-138">CommonParameters</span></span>
<span data-ttu-id="abf89-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf89-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abf89-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf89-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abf89-141">INPUTS</span></span>

### <span data-ttu-id="abf89-142">System. String</span><span class="sxs-lookup"><span data-stu-id="abf89-142">System.String</span></span>

### <span data-ttu-id="abf89-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="abf89-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="abf89-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="abf89-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="abf89-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abf89-145">OUTPUTS</span></span>

### <span data-ttu-id="abf89-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="abf89-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="abf89-147">Note</span><span class="sxs-lookup"><span data-stu-id="abf89-147">NOTES</span></span>

## <span data-ttu-id="abf89-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abf89-148">RELATED LINKS</span></span>
