---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 3e2e04e2e489b9c9322c62d1c7006490d7bf9bd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957613"
---
# <span data-ttu-id="4c597-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4c597-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="4c597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c597-102">SYNOPSIS</span></span>
<span data-ttu-id="4c597-103">Crea un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="4c597-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="4c597-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c597-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c597-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c597-105">DESCRIPTION</span></span>
<span data-ttu-id="4c597-106">Crea un set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="4c597-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="4c597-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c597-107">EXAMPLES</span></span>

### <span data-ttu-id="4c597-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c597-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="4c597-109">Crea un set di crittografia del disco usando la chiave attiva specificata nel vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="4c597-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="4c597-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c597-110">PARAMETERS</span></span>

### <span data-ttu-id="4c597-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c597-111">-AsJob</span></span>
<span data-ttu-id="4c597-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4c597-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c597-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c597-113">-DefaultProfile</span></span>
<span data-ttu-id="4c597-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c597-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c597-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c597-115">-InputObject</span></span>
<span data-ttu-id="4c597-116">Oggetto locale del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="4c597-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="4c597-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4c597-117">-Name</span></span>
<span data-ttu-id="4c597-118">Nome del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="4c597-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="4c597-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c597-119">-ResourceGroupName</span></span>
<span data-ttu-id="4c597-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c597-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4c597-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c597-121">-Confirm</span></span>
<span data-ttu-id="4c597-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c597-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c597-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c597-123">-WhatIf</span></span>
<span data-ttu-id="4c597-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c597-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c597-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c597-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c597-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c597-126">CommonParameters</span></span>
<span data-ttu-id="4c597-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c597-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c597-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c597-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c597-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c597-129">INPUTS</span></span>

### <span data-ttu-id="4c597-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4c597-130">System.String</span></span>

### <span data-ttu-id="4c597-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4c597-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="4c597-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c597-132">OUTPUTS</span></span>

### <span data-ttu-id="4c597-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4c597-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="4c597-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c597-134">NOTES</span></span>

## <span data-ttu-id="4c597-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c597-135">RELATED LINKS</span></span>
