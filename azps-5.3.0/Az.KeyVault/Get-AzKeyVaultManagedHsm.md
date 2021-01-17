---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476199"
---
# <span data-ttu-id="495ca-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="495ca-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="495ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="495ca-102">SYNOPSIS</span></span>
<span data-ttu-id="495ca-103">Ottenere i HSM gestiti.</span><span class="sxs-lookup"><span data-stu-id="495ca-103">Get managed HSMs.</span></span>

## <span data-ttu-id="495ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="495ca-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="495ca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="495ca-105">DESCRIPTION</span></span>
<span data-ttu-id="495ca-106">Il cmdlet **Get-AzKeyVaultManagedHsm** ottiene informazioni sulle HSM gestite in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="495ca-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="495ca-107">È possibile visualizzare tutte le istanze di HSM gestite in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un determinato HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="495ca-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="495ca-108">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet quando ricevi un singolo HSM gestito, dovresti farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="495ca-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="495ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="495ca-109">EXAMPLES</span></span>

### <span data-ttu-id="495ca-110">Esempio 1: ottenere tutti i HSM gestiti nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="495ca-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="495ca-111">Questo comando ottiene tutti i HSM gestiti nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="495ca-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="495ca-112">Esempio 2: ottenere un HSM gestito specifico</span><span class="sxs-lookup"><span data-stu-id="495ca-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="495ca-113">Questo comando ottiene l'HSM gestito denominato myhsm nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="495ca-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="495ca-114">Esempio 3: ottenere HSM gestiti in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="495ca-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="495ca-115">Questo comando ottiene tutti i HSM gestiti nel gruppo di risorse denominato myrg1.</span><span class="sxs-lookup"><span data-stu-id="495ca-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="495ca-116">Esempio 4: ottenere HSM gestiti tramite filtro</span><span class="sxs-lookup"><span data-stu-id="495ca-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="495ca-117">Questo comando ottiene tutti i HSM gestiti nell'abbonamento che iniziano con "myhsm".</span><span class="sxs-lookup"><span data-stu-id="495ca-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="495ca-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="495ca-118">PARAMETERS</span></span>

### <span data-ttu-id="495ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495ca-119">-DefaultProfile</span></span>
<span data-ttu-id="495ca-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="495ca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495ca-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="495ca-121">-Name</span></span>
<span data-ttu-id="495ca-122">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="495ca-122">HSM name.</span></span> <span data-ttu-id="495ca-123">Cmdlet costruisce l'FQDN di un HSM in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="495ca-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="495ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="495ca-125">Specifica il nome del gruppo di risorse associato all'HSM gestito in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="495ca-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

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

### <span data-ttu-id="495ca-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="495ca-126">-Tag</span></span>
<span data-ttu-id="495ca-127">Specifica la chiave e il valore facoltativo del tag specificato per filtrare l'elenco di HSM gestiti.</span><span class="sxs-lookup"><span data-stu-id="495ca-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="495ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495ca-128">CommonParameters</span></span>
<span data-ttu-id="495ca-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495ca-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="495ca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495ca-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="495ca-131">INPUTS</span></span>

### <span data-ttu-id="495ca-132">System. String</span><span class="sxs-lookup"><span data-stu-id="495ca-132">System.String</span></span>

### <span data-ttu-id="495ca-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="495ca-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="495ca-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="495ca-134">OUTPUTS</span></span>

### <span data-ttu-id="495ca-135">Microsoft. Azure. Commands. Vault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="495ca-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="495ca-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="495ca-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="495ca-137">Note</span><span class="sxs-lookup"><span data-stu-id="495ca-137">NOTES</span></span>

## <span data-ttu-id="495ca-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="495ca-138">RELATED LINKS</span></span>

[<span data-ttu-id="495ca-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="495ca-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="495ca-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="495ca-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="495ca-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="495ca-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)