---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191357"
---
# <span data-ttu-id="f66ce-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f66ce-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="f66ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f66ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f66ce-103">Aggiorna un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="f66ce-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="f66ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f66ce-104">SYNTAX</span></span>

### <span data-ttu-id="f66ce-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f66ce-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f66ce-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f66ce-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f66ce-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f66ce-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f66ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f66ce-108">DESCRIPTION</span></span>
<span data-ttu-id="f66ce-109">Aggiorna un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="f66ce-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="f66ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f66ce-110">EXAMPLES</span></span>

### <span data-ttu-id="f66ce-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f66ce-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="f66ce-112">Aggiorna la crittografia del disco impostando la chiave attiva specificata nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="f66ce-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="f66ce-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f66ce-113">PARAMETERS</span></span>

### <span data-ttu-id="f66ce-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f66ce-114">-AsJob</span></span>
<span data-ttu-id="f66ce-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f66ce-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f66ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66ce-116">-DefaultProfile</span></span>
<span data-ttu-id="f66ce-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f66ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f66ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f66ce-118">-InputObject</span></span>
<span data-ttu-id="f66ce-119">Oggetto local del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="f66ce-119">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="f66ce-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="f66ce-120">-KeyUrl</span></span>
<span data-ttu-id="f66ce-121">URL che punta alla chiave attiva in Key Vault</span><span class="sxs-lookup"><span data-stu-id="f66ce-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="f66ce-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f66ce-122">-Name</span></span>
<span data-ttu-id="f66ce-123">Nome del set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="f66ce-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="f66ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f66ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="f66ce-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f66ce-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f66ce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f66ce-126">-ResourceId</span></span>
<span data-ttu-id="f66ce-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f66ce-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="f66ce-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f66ce-128">-SourceVaultId</span></span>
<span data-ttu-id="f66ce-129">ID risorsa del caveau contenente il tasto attivo.</span><span class="sxs-lookup"><span data-stu-id="f66ce-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="f66ce-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f66ce-130">-Tag</span></span>
<span data-ttu-id="f66ce-131">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f66ce-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f66ce-132">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f66ce-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f66ce-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f66ce-133">-Confirm</span></span>
<span data-ttu-id="f66ce-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f66ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f66ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f66ce-135">-WhatIf</span></span>
<span data-ttu-id="f66ce-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f66ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f66ce-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f66ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f66ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66ce-138">CommonParameters</span></span>
<span data-ttu-id="f66ce-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66ce-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f66ce-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66ce-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f66ce-141">INPUTS</span></span>

### <span data-ttu-id="f66ce-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f66ce-142">System.String</span></span>

### <span data-ttu-id="f66ce-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f66ce-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="f66ce-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f66ce-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f66ce-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f66ce-145">OUTPUTS</span></span>

### <span data-ttu-id="f66ce-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f66ce-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="f66ce-147">Note</span><span class="sxs-lookup"><span data-stu-id="f66ce-147">NOTES</span></span>

## <span data-ttu-id="f66ce-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f66ce-148">RELATED LINKS</span></span>