---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: b65fed5670f34072504c736283ba12e51086d3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995481"
---
# <span data-ttu-id="e09df-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e09df-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="e09df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09df-102">SYNOPSIS</span></span>
<span data-ttu-id="e09df-103">Ottenere ims gestiti.</span><span class="sxs-lookup"><span data-stu-id="e09df-103">Get managed HSMs.</span></span>

## <span data-ttu-id="e09df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e09df-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e09df-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e09df-105">DESCRIPTION</span></span>
<span data-ttu-id="e09df-106">Il cmdlet **Get-AzKeyVaultManagedHsm** ottiene informazioni sui messaggi HMS gestiti in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="e09df-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="e09df-107">È possibile visualizzare tutte le istanze di HMS gestite in una sottoscrizione oppure filtrare i risultati in base a un gruppo di risorse o a un determinato HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="e09df-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="e09df-108">Anche se è facoltativo specificare il gruppo di risorse per questo cmdlet quando si ottiene un unico HSM gestito, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e09df-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="e09df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e09df-109">EXAMPLES</span></span>

### <span data-ttu-id="e09df-110">Esempio 1: Ottenere tutti i file HMS gestiti nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e09df-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e09df-111">Questo comando recupera tutti i file HMS gestiti nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e09df-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="e09df-112">Esempio 2: Ottenere uno specifico HSM gestito</span><span class="sxs-lookup"><span data-stu-id="e09df-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e09df-113">Questo comando recupera l'HSM gestito denominato myhsm nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e09df-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="e09df-114">Esempio 3: Ottenere i file HMS gestiti in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e09df-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e09df-115">Questo comando recupera tutti i file HMS gestiti nel gruppo di risorse denominato myrg1.</span><span class="sxs-lookup"><span data-stu-id="e09df-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="e09df-116">Esempio 4: Usare i filtri per ottenere messaggi HMS gestiti</span><span class="sxs-lookup"><span data-stu-id="e09df-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e09df-117">Questo comando recupera tutti gli HMS gestiti nell'abbonamento che iniziano con "myhsm".</span><span class="sxs-lookup"><span data-stu-id="e09df-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="e09df-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e09df-118">PARAMETERS</span></span>

### <span data-ttu-id="e09df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09df-119">-DefaultProfile</span></span>
<span data-ttu-id="e09df-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e09df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e09df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e09df-121">-Name</span></span>
<span data-ttu-id="e09df-122">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="e09df-122">HSM name.</span></span> <span data-ttu-id="e09df-123">Il cmdlet crea l'FQDN di un servizio HSM in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="e09df-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e09df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e09df-124">-ResourceGroupName</span></span>
<span data-ttu-id="e09df-125">Specifica il nome del gruppo di risorse associato al servizio HSM gestito in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="e09df-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e09df-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="e09df-126">-Tag</span></span>
<span data-ttu-id="e09df-127">Specifica la chiave e il valore facoltativo del tag specificato in base a cui filtrare l'elenco di messaggi hms gestiti.</span><span class="sxs-lookup"><span data-stu-id="e09df-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="e09df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09df-128">CommonParameters</span></span>
<span data-ttu-id="e09df-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e09df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09df-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e09df-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09df-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e09df-131">INPUTS</span></span>

### <span data-ttu-id="e09df-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e09df-132">System.String</span></span>

### <span data-ttu-id="e09df-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e09df-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e09df-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e09df-134">OUTPUTS</span></span>

### <span data-ttu-id="e09df-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e09df-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="e09df-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e09df-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="e09df-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e09df-137">NOTES</span></span>

## <span data-ttu-id="e09df-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e09df-138">RELATED LINKS</span></span>

[<span data-ttu-id="e09df-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e09df-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="e09df-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e09df-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="e09df-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e09df-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)