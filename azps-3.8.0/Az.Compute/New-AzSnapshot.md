---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f22a5b4bc9b30e152827f1914bd03a4a6cee4971
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019406"
---
# <span data-ttu-id="5d04a-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="5d04a-101">New-AzSnapshot</span></span>

## <span data-ttu-id="5d04a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d04a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d04a-103">Crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="5d04a-103">Creates a snapshot.</span></span>

## <span data-ttu-id="5d04a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d04a-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d04a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d04a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d04a-106">Il cmdlet **New-AzSnapshot** crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="5d04a-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="5d04a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d04a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d04a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d04a-108">Example 1</span></span>
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

<span data-ttu-id="5d04a-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5d04a-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="5d04a-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="5d04a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5d04a-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="5d04a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="5d04a-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5d04a-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5d04a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d04a-113">PARAMETERS</span></span>

### <span data-ttu-id="5d04a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d04a-114">-AsJob</span></span>
<span data-ttu-id="5d04a-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="5d04a-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5d04a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d04a-116">-DefaultProfile</span></span>
<span data-ttu-id="5d04a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d04a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d04a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d04a-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d04a-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d04a-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5d04a-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="5d04a-120">-Snapshot</span></span>
<span data-ttu-id="5d04a-121">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="5d04a-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="5d04a-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5d04a-122">-SnapshotName</span></span>
<span data-ttu-id="5d04a-123">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="5d04a-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5d04a-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5d04a-124">-Confirm</span></span>
<span data-ttu-id="5d04a-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d04a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d04a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d04a-126">-WhatIf</span></span>
<span data-ttu-id="5d04a-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d04a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d04a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d04a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d04a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d04a-129">CommonParameters</span></span>
<span data-ttu-id="5d04a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d04a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d04a-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d04a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d04a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d04a-132">INPUTS</span></span>

### <span data-ttu-id="5d04a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5d04a-133">System.String</span></span>

### <span data-ttu-id="5d04a-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="5d04a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="5d04a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d04a-135">OUTPUTS</span></span>

### <span data-ttu-id="5d04a-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="5d04a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="5d04a-137">Note</span><span class="sxs-lookup"><span data-stu-id="5d04a-137">NOTES</span></span>

## <span data-ttu-id="5d04a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d04a-138">RELATED LINKS</span></span>
