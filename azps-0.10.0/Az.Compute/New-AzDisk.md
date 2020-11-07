---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1eea8504f974e7ffc504520a5b5abc036c4d3e2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863662"
---
# <span data-ttu-id="90b54-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="90b54-101">New-AzDisk</span></span>

## <span data-ttu-id="90b54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90b54-102">SYNOPSIS</span></span>
<span data-ttu-id="90b54-103">Crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="90b54-103">Creates a managed disk.</span></span>

## <span data-ttu-id="90b54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90b54-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b54-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90b54-105">DESCRIPTION</span></span>
<span data-ttu-id="90b54-106">Il cmdlet **New-AzDisk** crea un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="90b54-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="90b54-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90b54-107">EXAMPLES</span></span>

### <span data-ttu-id="90b54-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90b54-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="90b54-109">Il primo comando crea un oggetto disco locale vuoto con la dimensione 5GB in Standard_LRS tipo di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="90b54-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="90b54-110">Imposta anche il tipo di sistema operativo Windows e Abilita le impostazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="90b54-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="90b54-111">Il secondo e il terzo comando impostano le impostazioni della chiave di crittografia del disco e della chiave di crittografia per l'oggetto disco.</span><span class="sxs-lookup"><span data-stu-id="90b54-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="90b54-112">L'ultimo comando accetta l'oggetto disk e crea un disco con il nome "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="90b54-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="90b54-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90b54-113">PARAMETERS</span></span>

### <span data-ttu-id="90b54-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90b54-114">-AsJob</span></span>
<span data-ttu-id="90b54-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="90b54-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="90b54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b54-116">-DefaultProfile</span></span>
<span data-ttu-id="90b54-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90b54-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b54-118">-Disco</span><span class="sxs-lookup"><span data-stu-id="90b54-118">-Disk</span></span>
<span data-ttu-id="90b54-119">Specifica un oggetto disco locale.</span><span class="sxs-lookup"><span data-stu-id="90b54-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90b54-120">-Diskname</span><span class="sxs-lookup"><span data-stu-id="90b54-120">-DiskName</span></span>
<span data-ttu-id="90b54-121">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="90b54-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="90b54-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b54-122">-ResourceGroupName</span></span>
<span data-ttu-id="90b54-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90b54-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90b54-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90b54-124">-Confirm</span></span>
<span data-ttu-id="90b54-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90b54-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b54-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b54-126">-WhatIf</span></span>
<span data-ttu-id="90b54-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90b54-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b54-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90b54-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b54-129">CommonParameters</span></span>
<span data-ttu-id="90b54-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b54-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b54-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b54-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90b54-132">INPUTS</span></span>

### <span data-ttu-id="90b54-133">System. String</span><span class="sxs-lookup"><span data-stu-id="90b54-133">System.String</span></span>
<span data-ttu-id="90b54-134">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="90b54-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="90b54-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90b54-135">OUTPUTS</span></span>

### <span data-ttu-id="90b54-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="90b54-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="90b54-137">Note</span><span class="sxs-lookup"><span data-stu-id="90b54-137">NOTES</span></span>

## <span data-ttu-id="90b54-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90b54-138">RELATED LINKS</span></span>

