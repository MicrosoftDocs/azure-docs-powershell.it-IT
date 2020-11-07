---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: c88365a64c9102b74811fedb2d93e103346e5a50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675059"
---
# <span data-ttu-id="f4e87-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="f4e87-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="f4e87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4e87-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e87-103">Crea un nuovo processo di databox con i parametri specificati</span><span class="sxs-lookup"><span data-stu-id="f4e87-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="f4e87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4e87-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4e87-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e87-106">Il cmdlet **New-AzDataBoxJob** viene usato per creare un nuovo processo di databox specificando i dettagli necessari per la creazione del processo.</span><span class="sxs-lookup"><span data-stu-id="f4e87-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="f4e87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4e87-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e87-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4e87-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="f4e87-109">Il cmdlet accetta tutti i parametri necessari e alcuni parametri facoltativi per creare il processo databox.</span><span class="sxs-lookup"><span data-stu-id="f4e87-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="f4e87-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4e87-110">PARAMETERS</span></span>

### <span data-ttu-id="f4e87-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="f4e87-111">-AddressType</span></span>
<span data-ttu-id="f4e87-112">Tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="f4e87-112">Type of Address.</span></span> <span data-ttu-id="f4e87-113">Valori disponibili: AddressType. None (impostazione predefinita), AddressType. Residential, AddressType. Commercial</span><span class="sxs-lookup"><span data-stu-id="f4e87-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-114">-Città</span><span class="sxs-lookup"><span data-stu-id="f4e87-114">-City</span></span>
<span data-ttu-id="f4e87-115">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="f4e87-115">Name of the City.</span></span> <span data-ttu-id="f4e87-116">Es: San Francisco</span><span class="sxs-lookup"><span data-stu-id="f4e87-116">Ex : San Francisco</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="f4e87-117">-CompanyName</span></span>
<span data-ttu-id="f4e87-118">Nome della società</span><span class="sxs-lookup"><span data-stu-id="f4e87-118">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="f4e87-119">-ContactName</span></span>
<span data-ttu-id="f4e87-120">Nome contatto</span><span class="sxs-lookup"><span data-stu-id="f4e87-120">Contact Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="f4e87-121">-CountryCode</span></span>
<span data-ttu-id="f4e87-122">Codice paese.</span><span class="sxs-lookup"><span data-stu-id="f4e87-122">Country Code.</span></span> <span data-ttu-id="f4e87-123">Es: Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="f4e87-123">Ex: US</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="f4e87-124">-DataBoxType</span></span>
<span data-ttu-id="f4e87-125">Tipo SKU di databox.</span><span class="sxs-lookup"><span data-stu-id="f4e87-125">Sku type of Databox.</span></span>  <span data-ttu-id="f4e87-126">Valori disponibili: DataBoxDisk, databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="f4e87-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e87-127">-DefaultProfile</span></span>
<span data-ttu-id="f4e87-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e87-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e87-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="f4e87-129">-EmailId</span></span>
<span data-ttu-id="f4e87-130">È possibile fornire l'elenco di EmailIds.</span><span class="sxs-lookup"><span data-stu-id="f4e87-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="f4e87-131">Atleast uno è obbligatorio</span><span class="sxs-lookup"><span data-stu-id="f4e87-131">Atleast one is mandatory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="f4e87-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="f4e87-133">Per l'ordine di DataBoxDisk, specificare i dati previsti in terabyte è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f4e87-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f4e87-134">-Location</span></span>
<span data-ttu-id="f4e87-135">Posizione dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="f4e87-135">Location of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4e87-136">-Name</span></span>
<span data-ttu-id="f4e87-137">Nome del processo di databox da creare</span><span class="sxs-lookup"><span data-stu-id="f4e87-137">Name of the databox job to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="f4e87-138">-PhoneNumber</span></span>
<span data-ttu-id="f4e87-139">Numero di contatto</span><span class="sxs-lookup"><span data-stu-id="f4e87-139">Contact Number</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-140">-Cap</span><span class="sxs-lookup"><span data-stu-id="f4e87-140">-PostalCode</span></span>
<span data-ttu-id="f4e87-141">Codice postale</span><span class="sxs-lookup"><span data-stu-id="f4e87-141">Postal Code</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e87-142">-ResourceGroupName</span></span>
<span data-ttu-id="f4e87-143">Nome del gruppo di risorse in cui deve essere creato il processo databox.</span><span class="sxs-lookup"><span data-stu-id="f4e87-143">Resource Group Name under which the databox job has to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="f4e87-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="f4e87-145">Immettere il codice stato o provincia.</span><span class="sxs-lookup"><span data-stu-id="f4e87-145">Input the state or province code.</span></span> <span data-ttu-id="f4e87-146">Come CA-California; FL-Florida; NY-New York</span><span class="sxs-lookup"><span data-stu-id="f4e87-146">Like CA - California; FL - Florida; NY - New York</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f4e87-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="f4e87-148">Elenco di ID delle risorse degli account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f4e87-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="f4e87-149">Atleast uno è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f4e87-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="f4e87-150">-StreetAddress1</span></span>
<span data-ttu-id="f4e87-151">Indirizzo di strada</span><span class="sxs-lookup"><span data-stu-id="f4e87-151">Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="f4e87-152">-StreetAddress2</span></span>
<span data-ttu-id="f4e87-153">Indirizzo di strada aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="f4e87-153">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="f4e87-154">-StreetAddress3</span></span>
<span data-ttu-id="f4e87-155">Indirizzo di strada aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="f4e87-155">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e87-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4e87-156">-Confirm</span></span>
<span data-ttu-id="f4e87-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4e87-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e87-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e87-158">-WhatIf</span></span>
<span data-ttu-id="f4e87-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4e87-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4e87-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4e87-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e87-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e87-161">CommonParameters</span></span>
<span data-ttu-id="f4e87-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e87-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e87-163">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4e87-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e87-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4e87-164">INPUTS</span></span>

### <span data-ttu-id="f4e87-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="f4e87-165">System.String[]</span></span>

## <span data-ttu-id="f4e87-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4e87-166">OUTPUTS</span></span>

### <span data-ttu-id="f4e87-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="f4e87-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="f4e87-168">Note</span><span class="sxs-lookup"><span data-stu-id="f4e87-168">NOTES</span></span>

## <span data-ttu-id="f4e87-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4e87-169">RELATED LINKS</span></span>
