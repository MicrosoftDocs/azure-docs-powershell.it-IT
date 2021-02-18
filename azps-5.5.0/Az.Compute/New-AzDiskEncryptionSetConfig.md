---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181646"
---
# <span data-ttu-id="3128d-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="3128d-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="3128d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3128d-102">SYNOPSIS</span></span>
<span data-ttu-id="3128d-103">Crea un oggetto set di crittografia disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="3128d-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="3128d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3128d-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3128d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3128d-105">DESCRIPTION</span></span>
<span data-ttu-id="3128d-106">Crea un oggetto set di crittografia disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="3128d-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="3128d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3128d-107">EXAMPLES</span></span>

### <span data-ttu-id="3128d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3128d-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="3128d-109">Crea un set di crittografia del disco usando la chiave attiva specificata nel vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="3128d-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="3128d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3128d-110">PARAMETERS</span></span>

### <span data-ttu-id="3128d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3128d-111">-DefaultProfile</span></span>
<span data-ttu-id="3128d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3128d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3128d-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="3128d-113">-EncryptionType</span></span>
<span data-ttu-id="3128d-114">Consente di impostare il tipo di crittografia del set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="3128d-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="3128d-115">I valori disponibili sono: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span><span class="sxs-lookup"><span data-stu-id="3128d-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="3128d-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3128d-116">-IdentityType</span></span>
<span data-ttu-id="3128d-117">Tipo di identità gestita usata da DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="3128d-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="3128d-118">È supportato solo SystemAssigned.</span><span class="sxs-lookup"><span data-stu-id="3128d-118">Only SystemAssigned is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3128d-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="3128d-119">-KeyUrl</span></span>
<span data-ttu-id="3128d-120">URL che punta alla chiave attiva in KeyVault</span><span class="sxs-lookup"><span data-stu-id="3128d-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="3128d-121">-Location</span><span class="sxs-lookup"><span data-stu-id="3128d-121">-Location</span></span>
<span data-ttu-id="3128d-122">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="3128d-122">Specifies a location.</span></span>

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

### <span data-ttu-id="3128d-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3128d-123">-SourceVaultId</span></span>
<span data-ttu-id="3128d-124">ID risorsa della chiaveVault contenente la chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="3128d-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3128d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3128d-125">-Tag</span></span>
<span data-ttu-id="3128d-126">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3128d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3128d-127">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3128d-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3128d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3128d-128">-Confirm</span></span>
<span data-ttu-id="3128d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3128d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3128d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3128d-130">-WhatIf</span></span>
<span data-ttu-id="3128d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3128d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3128d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3128d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3128d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3128d-133">CommonParameters</span></span>
<span data-ttu-id="3128d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3128d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3128d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3128d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3128d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="3128d-136">INPUTS</span></span>

### <span data-ttu-id="3128d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3128d-137">System.String</span></span>

### <span data-ttu-id="3128d-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3128d-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3128d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3128d-139">OUTPUTS</span></span>

### <span data-ttu-id="3128d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3128d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="3128d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="3128d-141">NOTES</span></span>

## <span data-ttu-id="3128d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3128d-142">RELATED LINKS</span></span>
