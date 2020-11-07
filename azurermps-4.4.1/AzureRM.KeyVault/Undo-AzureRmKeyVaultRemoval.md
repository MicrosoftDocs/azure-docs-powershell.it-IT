---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687183"
---
# <span data-ttu-id="64f4a-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="64f4a-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="64f4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="64f4a-103">Ripristina un Vault di chiave eliminata in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="64f4a-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64f4a-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64f4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="64f4a-106">Il cmdlet **Undo-AzureRmKeyVaultRemoval** recupererà un Vault chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="64f4a-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="64f4a-107">Il Vault recuperato sarà attivo dopo il ripristino</span><span class="sxs-lookup"><span data-stu-id="64f4a-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="64f4a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64f4a-108">EXAMPLES</span></span>

### <span data-ttu-id="64f4a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64f4a-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="64f4a-110">Questo comando recupererà il Vault Key "MyKeyVault" eliminato in precedenza da eastus2 Region e il gruppo di risorse "MyResourceGroup" in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="64f4a-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="64f4a-111">Sostituisce anche i tag con il nuovo tag.</span><span class="sxs-lookup"><span data-stu-id="64f4a-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="64f4a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64f4a-112">PARAMETERS</span></span>

### <span data-ttu-id="64f4a-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="64f4a-113">-Location</span></span>
<span data-ttu-id="64f4a-114">Specifica l'area di Azure originale del Vault eliminata.</span><span class="sxs-lookup"><span data-stu-id="64f4a-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f4a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f4a-115">-ResourceGroupName</span></span>
<span data-ttu-id="64f4a-116">Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="64f4a-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f4a-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="64f4a-117">-Tag</span></span>
<span data-ttu-id="64f4a-118">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="64f4a-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="64f4a-119">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="64f4a-119">For example:</span></span>

<span data-ttu-id="64f4a-120">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="64f4a-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f4a-121">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="64f4a-121">-VaultName</span></span>
<span data-ttu-id="64f4a-122">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="64f4a-122">Vault name.</span></span>
<span data-ttu-id="64f4a-123">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="64f4a-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="64f4a-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64f4a-124">-Confirm</span></span>
<span data-ttu-id="64f4a-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64f4a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f4a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f4a-126">-WhatIf</span></span>
<span data-ttu-id="64f4a-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64f4a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64f4a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64f4a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f4a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f4a-129">-DefaultProfile</span></span>
<span data-ttu-id="64f4a-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64f4a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f4a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f4a-131">CommonParameters</span></span>
<span data-ttu-id="64f4a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f4a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f4a-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f4a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f4a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64f4a-134">INPUTS</span></span>

### <span data-ttu-id="64f4a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="64f4a-135">System.String</span></span>
<span data-ttu-id="64f4a-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64f4a-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64f4a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64f4a-137">OUTPUTS</span></span>

### <span data-ttu-id="64f4a-138">Microsoft. Azure. Commands. Vault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="64f4a-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="64f4a-139">Note</span><span class="sxs-lookup"><span data-stu-id="64f4a-139">NOTES</span></span>

## <span data-ttu-id="64f4a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64f4a-140">RELATED LINKS</span></span>

[<span data-ttu-id="64f4a-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="64f4a-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="64f4a-142">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="64f4a-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="64f4a-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="64f4a-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
