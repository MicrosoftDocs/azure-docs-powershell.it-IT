---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f22a5b4bc9b30e152827f1914bd03a4a6cee4971
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204874"
---
# <span data-ttu-id="e812e-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="e812e-101">New-AzSnapshot</span></span>

## <span data-ttu-id="e812e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e812e-102">SYNOPSIS</span></span>
<span data-ttu-id="e812e-103">Crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="e812e-103">Creates a snapshot.</span></span>

## <span data-ttu-id="e812e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e812e-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e812e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e812e-105">DESCRIPTION</span></span>
<span data-ttu-id="e812e-106">Il cmdlet **New-AzSnapshot** crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="e812e-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="e812e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e812e-107">EXAMPLES</span></span>

### <span data-ttu-id="e812e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e812e-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="e812e-109">Il primo comando crea un oggetto snapshot vuoto locale con dimensioni di 5 GB Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e812e-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="e812e-110">Configura anche il tipo di sistema operativo Windows e abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e812e-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e812e-111">Il secondo e il terzo comando impostano la chiave di crittografia disco e le relative impostazioni per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="e812e-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="e812e-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome 'Snapshot01' nel gruppo di risorse 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="e812e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e812e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e812e-113">PARAMETERS</span></span>

### <span data-ttu-id="e812e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e812e-114">-AsJob</span></span>
<span data-ttu-id="e812e-115">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e812e-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e812e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e812e-116">-DefaultProfile</span></span>
<span data-ttu-id="e812e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e812e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e812e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e812e-118">-ResourceGroupName</span></span>
<span data-ttu-id="e812e-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e812e-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e812e-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="e812e-120">-Snapshot</span></span>
<span data-ttu-id="e812e-121">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="e812e-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e812e-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e812e-122">-SnapshotName</span></span>
<span data-ttu-id="e812e-123">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="e812e-123">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e812e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e812e-124">-Confirm</span></span>
<span data-ttu-id="e812e-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e812e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e812e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e812e-126">-WhatIf</span></span>
<span data-ttu-id="e812e-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e812e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e812e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e812e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e812e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e812e-129">CommonParameters</span></span>
<span data-ttu-id="e812e-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e812e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e812e-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e812e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e812e-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e812e-132">INPUTS</span></span>

### <span data-ttu-id="e812e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e812e-133">System.String</span></span>

### <span data-ttu-id="e812e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="e812e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="e812e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e812e-135">OUTPUTS</span></span>

### <span data-ttu-id="e812e-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="e812e-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="e812e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e812e-137">NOTES</span></span>

## <span data-ttu-id="e812e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e812e-138">RELATED LINKS</span></span>
