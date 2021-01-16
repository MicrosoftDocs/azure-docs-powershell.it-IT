---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337015"
---
# <span data-ttu-id="1c793-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1c793-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="1c793-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c793-102">SYNOPSIS</span></span>
<span data-ttu-id="1c793-103">Crea un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="1c793-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="1c793-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c793-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c793-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c793-105">DESCRIPTION</span></span>
<span data-ttu-id="1c793-106">Il cmdlet **New-AzKeyVaultManagedHsm** crea un HSM gestito nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1c793-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="1c793-107">Per aggiungere, rimuovere o elencare le chiavi nell'HSM gestito, l'utente deve concedere le autorizzazioni aggiungendo l'ID utente all'amministratore.</span><span class="sxs-lookup"><span data-stu-id="1c793-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="1c793-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c793-108">EXAMPLES</span></span>

### <span data-ttu-id="1c793-109">Esempio 1: creare un HSM gestito StandardB1</span><span class="sxs-lookup"><span data-stu-id="1c793-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1c793-110">Questo comando crea un HSM gestito denominato myhsm nella posizione eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="1c793-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="1c793-111">Il comando aggiunge l'HSM gestito al gruppo di risorse denominato myrg1.</span><span class="sxs-lookup"><span data-stu-id="1c793-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="1c793-112">Poiché il comando non specifica un valore per il parametro *SKU* , crea un Standard_B1 HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="1c793-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="1c793-113">Esempio 2: creare un HSM gestito CustomB32</span><span class="sxs-lookup"><span data-stu-id="1c793-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="1c793-114">Questo comando crea un HSM gestito, proprio come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="1c793-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="1c793-115">Tuttavia, specifica un valore di CustomB32 per il parametro *SKU* per creare un HSM gestito CustomB32.</span><span class="sxs-lookup"><span data-stu-id="1c793-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="1c793-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c793-116">PARAMETERS</span></span>

### <span data-ttu-id="1c793-117">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="1c793-117">-Administrator</span></span>
<span data-ttu-id="1c793-118">ID oggetto amministratore iniziale per questo pool di HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="1c793-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="1c793-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c793-119">-AsJob</span></span>
<span data-ttu-id="1c793-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1c793-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c793-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c793-121">-DefaultProfile</span></span>
<span data-ttu-id="1c793-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c793-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c793-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1c793-123">-Location</span></span>
<span data-ttu-id="1c793-124">Specifica l'area di Azure in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1c793-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="1c793-125">Usa il comando Get-AzResourceProvider con il parametro ProviderNamespace per visualizzare le tue scelte.</span><span class="sxs-lookup"><span data-stu-id="1c793-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="1c793-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c793-126">-Name</span></span>
<span data-ttu-id="1c793-127">Specifica un nome dell'HSM gestito da creare.</span><span class="sxs-lookup"><span data-stu-id="1c793-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="1c793-128">Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="1c793-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="1c793-129">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="1c793-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="1c793-130">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="1c793-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="1c793-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c793-131">-ResourceGroupName</span></span>
<span data-ttu-id="1c793-132">Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1c793-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="1c793-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="1c793-133">-Sku</span></span>
<span data-ttu-id="1c793-134">Specifica l'USK dell'istanza di HSM gestita.</span><span class="sxs-lookup"><span data-stu-id="1c793-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="1c793-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c793-135">-Tag</span></span>
<span data-ttu-id="1c793-136">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1c793-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1c793-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c793-137">-Confirm</span></span>
<span data-ttu-id="1c793-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c793-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c793-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c793-139">-WhatIf</span></span>
<span data-ttu-id="1c793-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c793-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c793-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c793-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c793-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c793-142">CommonParameters</span></span>
<span data-ttu-id="1c793-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c793-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c793-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c793-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c793-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c793-145">INPUTS</span></span>

### <span data-ttu-id="1c793-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1c793-146">System.String</span></span>

### <span data-ttu-id="1c793-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="1c793-147">System.String[]</span></span>

### <span data-ttu-id="1c793-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c793-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1c793-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c793-149">OUTPUTS</span></span>

### <span data-ttu-id="1c793-150">Microsoft. Azure. Commands. Vault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1c793-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="1c793-151">Note</span><span class="sxs-lookup"><span data-stu-id="1c793-151">NOTES</span></span>

## <span data-ttu-id="1c793-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c793-152">RELATED LINKS</span></span>

[<span data-ttu-id="1c793-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1c793-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1c793-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1c793-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1c793-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1c793-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)