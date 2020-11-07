---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: fa77808eddc0e51fa76a0883980b34552589f4ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866755"
---
# <span data-ttu-id="4bc34-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bc34-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="4bc34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bc34-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc34-103">Crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="4bc34-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bc34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bc34-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bc34-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc34-106">Il cmdlet **New-AzureRmSnapshot** crea uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="4bc34-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="4bc34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bc34-107">EXAMPLES</span></span>

### <span data-ttu-id="4bc34-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4bc34-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="4bc34-109">Il primo comando crea un oggetto snapshot locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4bc34-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="4bc34-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4bc34-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="4bc34-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto snapshot.</span><span class="sxs-lookup"><span data-stu-id="4bc34-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="4bc34-112">L'ultimo comando accetta l'oggetto snapshot e crea uno snapshot con il nome "Snapshot01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4bc34-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4bc34-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bc34-113">PARAMETERS</span></span>

### <span data-ttu-id="4bc34-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bc34-114">-AsJob</span></span>
<span data-ttu-id="4bc34-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4bc34-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc34-116">-DefaultProfile</span></span>
<span data-ttu-id="4bc34-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bc34-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc34-118">-ResourceGroupName</span></span>
<span data-ttu-id="4bc34-119">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4bc34-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc34-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="4bc34-120">-Snapshot</span></span>
<span data-ttu-id="4bc34-121">Specifica un oggetto snapshot locale.</span><span class="sxs-lookup"><span data-stu-id="4bc34-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc34-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4bc34-122">-SnapshotName</span></span>
<span data-ttu-id="4bc34-123">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="4bc34-123">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc34-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4bc34-124">-Confirm</span></span>
<span data-ttu-id="4bc34-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bc34-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc34-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc34-126">-WhatIf</span></span>
<span data-ttu-id="4bc34-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bc34-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc34-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bc34-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc34-129">CommonParameters</span></span>
<span data-ttu-id="4bc34-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc34-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc34-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc34-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bc34-132">INPUTS</span></span>

### <span data-ttu-id="4bc34-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4bc34-133">System.String</span></span>
<span data-ttu-id="4bc34-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bc34-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="4bc34-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bc34-135">OUTPUTS</span></span>

### <span data-ttu-id="4bc34-136">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bc34-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="4bc34-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="4bc34-137">System.Object</span></span>

## <span data-ttu-id="4bc34-138">Note</span><span class="sxs-lookup"><span data-stu-id="4bc34-138">NOTES</span></span>

## <span data-ttu-id="4bc34-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bc34-139">RELATED LINKS</span></span>

