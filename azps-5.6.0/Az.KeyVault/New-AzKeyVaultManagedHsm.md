---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 72804d546869f2d003813c8e69c067ad23966fa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001309"
---
# <span data-ttu-id="03a71-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="03a71-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="03a71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a71-102">SYNOPSIS</span></span>
<span data-ttu-id="03a71-103">Crea un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="03a71-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="03a71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03a71-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a71-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03a71-105">DESCRIPTION</span></span>
<span data-ttu-id="03a71-106">Il cmdlet **New-AzKeyVaultManagedHsm** crea un servizio HSM gestito nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="03a71-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="03a71-107">Per aggiungere, rimuovere o elencare le chiavi nell'HSM gestito, l'utente deve concedere le autorizzazioni aggiungendo l'ID utente all'amministratore.</span><span class="sxs-lookup"><span data-stu-id="03a71-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="03a71-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03a71-108">EXAMPLES</span></span>

### <span data-ttu-id="03a71-109">Esempio 1: Creare un HSM gestito da StandardB1</span><span class="sxs-lookup"><span data-stu-id="03a71-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="03a71-110">Questo comando crea un servizio HSM gestito denominato myhsm nella posizione eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="03a71-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="03a71-111">Il comando aggiunge il servizio HSM gestito al gruppo di risorse denominato myrg1.</span><span class="sxs-lookup"><span data-stu-id="03a71-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="03a71-112">Poiché il comando non specifica un valore per *il parametro SKU,* crea un Standard_B1 HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="03a71-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="03a71-113">Esempio 2: Creare un servizio HSM gestito da CustomB32</span><span class="sxs-lookup"><span data-stu-id="03a71-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="03a71-114">Questo comando crea un HSM gestito, come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="03a71-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="03a71-115">Tuttavia, specifica un valore CustomB32 per il parametro *SKU* per creare un HSM gestito da CustomB32.</span><span class="sxs-lookup"><span data-stu-id="03a71-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="03a71-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03a71-116">PARAMETERS</span></span>

### <span data-ttu-id="03a71-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="03a71-117">-Administrator</span></span>
<span data-ttu-id="03a71-118">ID oggetto amministratore iniziale per questo pool HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="03a71-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a71-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03a71-119">-AsJob</span></span>
<span data-ttu-id="03a71-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="03a71-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03a71-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a71-121">-DefaultProfile</span></span>
<span data-ttu-id="03a71-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03a71-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03a71-123">-Location</span><span class="sxs-lookup"><span data-stu-id="03a71-123">-Location</span></span>
<span data-ttu-id="03a71-124">Specifica l'area geografica di Azure in cui creare il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="03a71-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="03a71-125">Usare il comando Get-AzResourceProvider con il parametro ProviderNtassi per visualizzare le opzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="03a71-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="03a71-126">-Name</span><span class="sxs-lookup"><span data-stu-id="03a71-126">-Name</span></span>
<span data-ttu-id="03a71-127">Specifica un nome dell'HSM gestito da creare.</span><span class="sxs-lookup"><span data-stu-id="03a71-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="03a71-128">Il nome può essere qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="03a71-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="03a71-129">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="03a71-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="03a71-130">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="03a71-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a71-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a71-131">-ResourceGroupName</span></span>
<span data-ttu-id="03a71-132">Specifica il nome di un gruppo di risorse esistente in cui creare il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="03a71-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="03a71-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="03a71-133">-Sku</span></span>
<span data-ttu-id="03a71-134">Specifica lo SKU dell'istanza di HSM gestita.</span><span class="sxs-lookup"><span data-stu-id="03a71-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="03a71-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="03a71-135">-Tag</span></span>
<span data-ttu-id="03a71-136">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="03a71-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a71-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03a71-137">-Confirm</span></span>
<span data-ttu-id="03a71-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03a71-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a71-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a71-139">-WhatIf</span></span>
<span data-ttu-id="03a71-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03a71-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a71-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03a71-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a71-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a71-142">CommonParameters</span></span>
<span data-ttu-id="03a71-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a71-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a71-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03a71-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a71-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="03a71-145">INPUTS</span></span>

### <span data-ttu-id="03a71-146">System.String</span><span class="sxs-lookup"><span data-stu-id="03a71-146">System.String</span></span>

### <span data-ttu-id="03a71-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="03a71-147">System.String[]</span></span>

### <span data-ttu-id="03a71-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="03a71-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="03a71-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03a71-149">OUTPUTS</span></span>

### <span data-ttu-id="03a71-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="03a71-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="03a71-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="03a71-151">NOTES</span></span>

## <span data-ttu-id="03a71-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03a71-152">RELATED LINKS</span></span>

[<span data-ttu-id="03a71-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="03a71-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="03a71-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="03a71-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="03a71-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="03a71-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)