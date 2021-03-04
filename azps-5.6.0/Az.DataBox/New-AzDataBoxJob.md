---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 2c78f8b40621ba58b84169f2bd9022399fce80b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998674"
---
# <span data-ttu-id="6629f-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="6629f-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="6629f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6629f-102">SYNOPSIS</span></span>
<span data-ttu-id="6629f-103">Crea un nuovo processo databox usando i parametri specificati</span><span class="sxs-lookup"><span data-stu-id="6629f-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="6629f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6629f-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6629f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6629f-105">DESCRIPTION</span></span>
<span data-ttu-id="6629f-106">Il cmdlet **New-AzDataBoxJob** viene usato per creare un nuovo processo Databox specificando i dettagli necessari per la creazione del processo.</span><span class="sxs-lookup"><span data-stu-id="6629f-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="6629f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6629f-107">EXAMPLES</span></span>

### <span data-ttu-id="6629f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6629f-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="6629f-109">Il cmdlet accetta tutti i parametri obbligatori e alcuni parametri facoltativi per creare il processo della casella di dati.</span><span class="sxs-lookup"><span data-stu-id="6629f-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="6629f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6629f-110">PARAMETERS</span></span>

### <span data-ttu-id="6629f-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="6629f-111">-AddressType</span></span>
<span data-ttu-id="6629f-112">Tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="6629f-112">Type of Address.</span></span> <span data-ttu-id="6629f-113">Valori disponibili: AddressType.None (impostazione predefinita), AddressType.Residential, AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="6629f-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="6629f-114">-Città</span><span class="sxs-lookup"><span data-stu-id="6629f-114">-City</span></span>
<span data-ttu-id="6629f-115">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="6629f-115">Name of the City.</span></span> <span data-ttu-id="6629f-116">Ex : San Francisco</span><span class="sxs-lookup"><span data-stu-id="6629f-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="6629f-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="6629f-117">-CompanyName</span></span>
<span data-ttu-id="6629f-118">Nome della società</span><span class="sxs-lookup"><span data-stu-id="6629f-118">Name of the company</span></span>

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

### <span data-ttu-id="6629f-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="6629f-119">-ContactName</span></span>
<span data-ttu-id="6629f-120">Nome contatto</span><span class="sxs-lookup"><span data-stu-id="6629f-120">Contact Name</span></span>

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

### <span data-ttu-id="6629f-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="6629f-121">-CountryCode</span></span>
<span data-ttu-id="6629f-122">Codice paese.</span><span class="sxs-lookup"><span data-stu-id="6629f-122">Country Code.</span></span> <span data-ttu-id="6629f-123">Ad esempio: US</span><span class="sxs-lookup"><span data-stu-id="6629f-123">Ex: US</span></span>

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

### <span data-ttu-id="6629f-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="6629f-124">-DataBoxType</span></span>
<span data-ttu-id="6629f-125">Tipo di SKU della casella dati.</span><span class="sxs-lookup"><span data-stu-id="6629f-125">Sku type of Databox.</span></span>  <span data-ttu-id="6629f-126">Valori disponibili: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="6629f-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="6629f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6629f-127">-DefaultProfile</span></span>
<span data-ttu-id="6629f-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6629f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6629f-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="6629f-129">-EmailId</span></span>
<span data-ttu-id="6629f-130">È possibile specificare un elenco di EmailId.</span><span class="sxs-lookup"><span data-stu-id="6629f-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="6629f-131">Almeno uno è obbligatorio</span><span class="sxs-lookup"><span data-stu-id="6629f-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="6629f-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="6629f-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="6629f-133">Per l'ordine Disk di DataBox, specificare i dati previsti in terabyte è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6629f-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="6629f-134">-Location</span><span class="sxs-lookup"><span data-stu-id="6629f-134">-Location</span></span>
<span data-ttu-id="6629f-135">Luogo dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="6629f-135">Location of the subscription</span></span>

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

### <span data-ttu-id="6629f-136">-Name</span><span class="sxs-lookup"><span data-stu-id="6629f-136">-Name</span></span>
<span data-ttu-id="6629f-137">Nome del processo della casella di dati da creare</span><span class="sxs-lookup"><span data-stu-id="6629f-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="6629f-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6629f-138">-PhoneNumber</span></span>
<span data-ttu-id="6629f-139">Numero contatto</span><span class="sxs-lookup"><span data-stu-id="6629f-139">Contact Number</span></span> 

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

### <span data-ttu-id="6629f-140">-POSTALCode</span><span class="sxs-lookup"><span data-stu-id="6629f-140">-PostalCode</span></span>
<span data-ttu-id="6629f-141">CAP</span><span class="sxs-lookup"><span data-stu-id="6629f-141">Postal Code</span></span>

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

### <span data-ttu-id="6629f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6629f-142">-ResourceGroupName</span></span>
<span data-ttu-id="6629f-143">Nome gruppo di risorse in cui deve essere creato il processo della casella di dati.</span><span class="sxs-lookup"><span data-stu-id="6629f-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="6629f-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="6629f-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="6629f-145">Immettere il codice dello stato o della provincia.</span><span class="sxs-lookup"><span data-stu-id="6629f-145">Input the state or province code.</span></span> <span data-ttu-id="6629f-146">Like CA - California; FL - Florida; NY - New York</span><span class="sxs-lookup"><span data-stu-id="6629f-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="6629f-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6629f-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="6629f-148">Elenco degli ID risorsa degli account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6629f-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="6629f-149">Almeno uno è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6629f-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="6629f-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="6629f-150">-StreetAddress1</span></span>
<span data-ttu-id="6629f-151">Via e numero civico</span><span class="sxs-lookup"><span data-stu-id="6629f-151">Street Address</span></span>

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

### <span data-ttu-id="6629f-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="6629f-152">-StreetAddress2</span></span>
<span data-ttu-id="6629f-153">Via e numero civico aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="6629f-153">Additional Street Address</span></span>

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

### <span data-ttu-id="6629f-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="6629f-154">-StreetAddress3</span></span>
<span data-ttu-id="6629f-155">Via e numero civico aggiuntivo</span><span class="sxs-lookup"><span data-stu-id="6629f-155">Additional Street Address</span></span>

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

### <span data-ttu-id="6629f-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6629f-156">-Confirm</span></span>
<span data-ttu-id="6629f-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6629f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6629f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6629f-158">-WhatIf</span></span>
<span data-ttu-id="6629f-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6629f-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6629f-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6629f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6629f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6629f-161">CommonParameters</span></span>
<span data-ttu-id="6629f-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6629f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6629f-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6629f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6629f-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="6629f-164">INPUTS</span></span>

### <span data-ttu-id="6629f-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6629f-165">System.String[]</span></span>

## <span data-ttu-id="6629f-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6629f-166">OUTPUTS</span></span>

### <span data-ttu-id="6629f-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="6629f-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="6629f-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="6629f-168">NOTES</span></span>

## <span data-ttu-id="6629f-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6629f-169">RELATED LINKS</span></span>
