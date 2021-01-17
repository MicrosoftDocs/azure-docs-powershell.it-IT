---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322921"
---
# <span data-ttu-id="e0467-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e0467-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="e0467-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0467-102">SYNOPSIS</span></span>
<span data-ttu-id="e0467-103">Ruota la chiave di crittografia del disco del cluster HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="e0467-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="e0467-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0467-104">SYNTAX</span></span>

### <span data-ttu-id="e0467-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0467-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0467-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0467-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0467-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0467-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0467-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0467-108">DESCRIPTION</span></span>
<span data-ttu-id="e0467-109">Ruotare la chiave di crittografia del disco del cluster HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="e0467-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="e0467-110">Per questa operazione, il cluster deve avere accesso sia alla chiave corrente che alla nuova chiave prevista, in caso contrario l'operazione di rotazione dei tasti non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="e0467-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="e0467-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0467-111">EXAMPLES</span></span>

### <span data-ttu-id="e0467-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0467-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="e0467-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e0467-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="e0467-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0467-114">PARAMETERS</span></span>

### <span data-ttu-id="e0467-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0467-115">-DefaultProfile</span></span>
<span data-ttu-id="e0467-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0467-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0467-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="e0467-117">-EncryptionKeyName</span></span>
<span data-ttu-id="e0467-118">Ottiene o imposta il nome della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e0467-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="e0467-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e0467-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="e0467-120">Ottiene o imposta la versione della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e0467-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="e0467-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="e0467-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="e0467-122">Ottiene o imposta l'URI del Vault di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e0467-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="e0467-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0467-123">-InputObject</span></span>
<span data-ttu-id="e0467-124">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="e0467-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0467-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0467-125">-Name</span></span>
<span data-ttu-id="e0467-126">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e0467-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0467-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0467-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0467-128">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0467-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0467-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0467-129">-ResourceId</span></span>
<span data-ttu-id="e0467-130">Ottiene o imposta l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e0467-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0467-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0467-131">-Confirm</span></span>
<span data-ttu-id="e0467-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0467-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0467-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0467-133">-WhatIf</span></span>
<span data-ttu-id="e0467-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0467-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0467-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0467-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0467-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0467-136">CommonParameters</span></span>
<span data-ttu-id="e0467-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0467-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0467-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0467-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0467-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0467-139">INPUTS</span></span>

### <span data-ttu-id="e0467-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e0467-140">None</span></span>

## <span data-ttu-id="e0467-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0467-141">OUTPUTS</span></span>

### <span data-ttu-id="e0467-142">Microsoft. Azure. Management. HDInsight. Models. cluster</span><span class="sxs-lookup"><span data-stu-id="e0467-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="e0467-143">Note</span><span class="sxs-lookup"><span data-stu-id="e0467-143">NOTES</span></span>

## <span data-ttu-id="e0467-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0467-144">RELATED LINKS</span></span>

[<span data-ttu-id="e0467-145">Crittografia del disco di chiave gestita dal cliente</span><span class="sxs-lookup"><span data-stu-id="e0467-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
