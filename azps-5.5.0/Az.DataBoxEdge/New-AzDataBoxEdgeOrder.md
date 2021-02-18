---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181087"
---
# <span data-ttu-id="92f3e-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="92f3e-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="92f3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="92f3e-103">Crea un nuovo ordine per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92f3e-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="92f3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92f3e-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92f3e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="92f3e-106">Il cmdlet **New-AzDataBoxEdgeOrder** crea un nuovo ordine per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="92f3e-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="92f3e-107">Prima di creare un ordine, è necessario creare una risorsa dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="92f3e-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="92f3e-108">È possibile specificare dettagli come la persona di contatto, il nome della società, l'indirizzo di posta elettronica, l'indirizzo e così via come parametri per la creazione dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="92f3e-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="92f3e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92f3e-109">EXAMPLES</span></span>

### <span data-ttu-id="92f3e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92f3e-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="92f3e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92f3e-111">PARAMETERS</span></span>

### <span data-ttu-id="92f3e-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="92f3e-112">-AddressLine1</span></span>
<span data-ttu-id="92f3e-113">Indirizzo prima riga</span><span class="sxs-lookup"><span data-stu-id="92f3e-113">Address first line</span></span>

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

### <span data-ttu-id="92f3e-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="92f3e-114">-AddressLine2</span></span>
<span data-ttu-id="92f3e-115">Indirizzo seconda riga</span><span class="sxs-lookup"><span data-stu-id="92f3e-115">Address second line</span></span>

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

### <span data-ttu-id="92f3e-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="92f3e-116">-AddressLine3</span></span>
<span data-ttu-id="92f3e-117">Terza riga dell'indirizzo</span><span class="sxs-lookup"><span data-stu-id="92f3e-117">Address third line</span></span>

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

### <span data-ttu-id="92f3e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92f3e-118">-AsJob</span></span>
<span data-ttu-id="92f3e-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="92f3e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92f3e-120">-Città</span><span class="sxs-lookup"><span data-stu-id="92f3e-120">-City</span></span>
<span data-ttu-id="92f3e-121">Nome della città</span><span class="sxs-lookup"><span data-stu-id="92f3e-121">Name of the City</span></span>

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

### <span data-ttu-id="92f3e-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="92f3e-122">-CompanyName</span></span>
<span data-ttu-id="92f3e-123">Nome della società</span><span class="sxs-lookup"><span data-stu-id="92f3e-123">Name of the company</span></span>

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

### <span data-ttu-id="92f3e-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="92f3e-124">-ContactPerson</span></span>
<span data-ttu-id="92f3e-125">Nome della persona di contatto</span><span class="sxs-lookup"><span data-stu-id="92f3e-125">Name of the contact person</span></span>

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

### <span data-ttu-id="92f3e-126">-Paese</span><span class="sxs-lookup"><span data-stu-id="92f3e-126">-Country</span></span>
<span data-ttu-id="92f3e-127">Nome del paese</span><span class="sxs-lookup"><span data-stu-id="92f3e-127">Name of the Country</span></span>

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

### <span data-ttu-id="92f3e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f3e-128">-DefaultProfile</span></span>
<span data-ttu-id="92f3e-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92f3e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f3e-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="92f3e-130">-DeviceName</span></span>
<span data-ttu-id="92f3e-131">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="92f3e-131">Resource Name</span></span>

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

### <span data-ttu-id="92f3e-132">-E-mail</span><span class="sxs-lookup"><span data-stu-id="92f3e-132">-Email</span></span>
<span data-ttu-id="92f3e-133">Elenco dei messaggi di posta elettronica da ricevere gli aggiornamenti, accetta al massimo 10 messaggi di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="92f3e-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="92f3e-134">-Telefono</span><span class="sxs-lookup"><span data-stu-id="92f3e-134">-Phone</span></span>
<span data-ttu-id="92f3e-135">Numero di telefono della persona di contatto</span><span class="sxs-lookup"><span data-stu-id="92f3e-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="92f3e-136">-CAP</span><span class="sxs-lookup"><span data-stu-id="92f3e-136">-PostalCode</span></span>
<span data-ttu-id="92f3e-137">Codice postale dell'indirizzo</span><span class="sxs-lookup"><span data-stu-id="92f3e-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="92f3e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f3e-138">-ResourceGroupName</span></span>
<span data-ttu-id="92f3e-139">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="92f3e-139">Resource Group Name</span></span>

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

### <span data-ttu-id="92f3e-140">-State</span><span class="sxs-lookup"><span data-stu-id="92f3e-140">-State</span></span>
<span data-ttu-id="92f3e-141">Nome dello stato</span><span class="sxs-lookup"><span data-stu-id="92f3e-141">Name of the State</span></span>

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

### <span data-ttu-id="92f3e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92f3e-142">-Confirm</span></span>
<span data-ttu-id="92f3e-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92f3e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92f3e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92f3e-144">-WhatIf</span></span>
<span data-ttu-id="92f3e-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92f3e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92f3e-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92f3e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92f3e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f3e-147">CommonParameters</span></span>
<span data-ttu-id="92f3e-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f3e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f3e-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92f3e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f3e-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="92f3e-150">INPUTS</span></span>

### <span data-ttu-id="92f3e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="92f3e-151">System.String</span></span>

## <span data-ttu-id="92f3e-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92f3e-152">OUTPUTS</span></span>

### <span data-ttu-id="92f3e-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="92f3e-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="92f3e-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="92f3e-154">NOTES</span></span>

## <span data-ttu-id="92f3e-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92f3e-155">RELATED LINKS</span></span>
