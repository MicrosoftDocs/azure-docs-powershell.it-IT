---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019425"
---
# <span data-ttu-id="6b3d8-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="6b3d8-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="6b3d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3d8-103">Crea un oggetto set di crittografia del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="6b3d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b3d8-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b3d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b3d8-105">DESCRIPTION</span></span>
<span data-ttu-id="6b3d8-106">Crea un oggetto set di crittografia del disco configurabile.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="6b3d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b3d8-107">EXAMPLES</span></span>

### <span data-ttu-id="6b3d8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b3d8-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="6b3d8-109">Crea la crittografia del disco impostata usando il tasto attivo indicato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="6b3d8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b3d8-110">PARAMETERS</span></span>

### <span data-ttu-id="6b3d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3d8-111">-DefaultProfile</span></span>
<span data-ttu-id="6b3d8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b3d8-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6b3d8-113">-IdentityType</span></span>
<span data-ttu-id="6b3d8-114">Tipo di identità gestita usata da DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="6b3d8-115">È supportato solo SystemAssigned.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-115">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="6b3d8-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="6b3d8-116">-KeyUrl</span></span>
<span data-ttu-id="6b3d8-117">URL che punta alla chiave attiva in Key Vault</span><span class="sxs-lookup"><span data-stu-id="6b3d8-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="6b3d8-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6b3d8-118">-Location</span></span>
<span data-ttu-id="6b3d8-119">Specifica una posizione.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-119">Specifies a location.</span></span>

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

### <span data-ttu-id="6b3d8-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6b3d8-120">-SourceVaultId</span></span>
<span data-ttu-id="6b3d8-121">ID risorsa del caveau contenente il tasto attivo.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-121">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="6b3d8-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b3d8-122">-Tag</span></span>
<span data-ttu-id="6b3d8-123">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6b3d8-124">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6b3d8-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6b3d8-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b3d8-125">-Confirm</span></span>
<span data-ttu-id="6b3d8-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3d8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3d8-127">-WhatIf</span></span>
<span data-ttu-id="6b3d8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b3d8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b3d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3d8-130">CommonParameters</span></span>
<span data-ttu-id="6b3d8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b3d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3d8-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b3d8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3d8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b3d8-133">INPUTS</span></span>

### <span data-ttu-id="6b3d8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6b3d8-134">System.String</span></span>

### <span data-ttu-id="6b3d8-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6b3d8-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6b3d8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b3d8-136">OUTPUTS</span></span>

### <span data-ttu-id="6b3d8-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6b3d8-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="6b3d8-138">Note</span><span class="sxs-lookup"><span data-stu-id="6b3d8-138">NOTES</span></span>

## <span data-ttu-id="6b3d8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b3d8-139">RELATED LINKS</span></span>
