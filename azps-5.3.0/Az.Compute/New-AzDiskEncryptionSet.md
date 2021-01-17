---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488423"
---
# <span data-ttu-id="ca372-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ca372-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="ca372-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca372-102">SYNOPSIS</span></span>
<span data-ttu-id="ca372-103">Crea un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="ca372-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="ca372-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca372-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca372-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca372-105">DESCRIPTION</span></span>
<span data-ttu-id="ca372-106">Crea un set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="ca372-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="ca372-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca372-107">EXAMPLES</span></span>

### <span data-ttu-id="ca372-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca372-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="ca372-109">Crea la crittografia del disco impostata usando il tasto attivo indicato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="ca372-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="ca372-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca372-110">PARAMETERS</span></span>

### <span data-ttu-id="ca372-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca372-111">-AsJob</span></span>
<span data-ttu-id="ca372-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca372-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca372-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca372-113">-DefaultProfile</span></span>
<span data-ttu-id="ca372-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca372-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca372-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca372-115">-InputObject</span></span>
<span data-ttu-id="ca372-116">Oggetto local del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="ca372-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca372-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca372-117">-Name</span></span>
<span data-ttu-id="ca372-118">Nome del set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="ca372-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca372-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca372-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca372-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca372-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ca372-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca372-121">-Confirm</span></span>
<span data-ttu-id="ca372-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca372-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca372-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca372-123">-WhatIf</span></span>
<span data-ttu-id="ca372-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca372-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca372-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca372-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca372-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca372-126">CommonParameters</span></span>
<span data-ttu-id="ca372-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca372-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca372-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca372-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca372-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca372-129">INPUTS</span></span>

### <span data-ttu-id="ca372-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ca372-130">System.String</span></span>

### <span data-ttu-id="ca372-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ca372-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="ca372-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca372-132">OUTPUTS</span></span>

### <span data-ttu-id="ca372-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="ca372-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="ca372-134">Note</span><span class="sxs-lookup"><span data-stu-id="ca372-134">NOTES</span></span>

## <span data-ttu-id="ca372-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca372-135">RELATED LINKS</span></span>
