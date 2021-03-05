---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 43a8d9969668abd96783fd766d4f99edb4b89e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994600"
---
# <span data-ttu-id="2e7f3-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2e7f3-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="2e7f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7f3-103">Crea un nuovo valore denominato.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-103">Creates new Named Value.</span></span>

## <span data-ttu-id="2e7f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e7f3-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e7f3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e7f3-105">DESCRIPTION</span></span>
<span data-ttu-id="2e7f3-106">Il cmdlet **New-AzApiManagementNamedValue** crea un valore denominato Gestione API **di** Azure.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="2e7f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e7f3-107">EXAMPLES</span></span>

### <span data-ttu-id="2e7f3-108">Esempio 1: Creare un valore denominato che include tag</span><span class="sxs-lookup"><span data-stu-id="2e7f3-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="2e7f3-109">Il primo comando assegna due valori alla variabile $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="2e7f3-110">Il secondo comando crea un valore denominato e assegna le stringhe nella $Tags come tag per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="2e7f3-111">Esempio 2: Creare un valore denominato con un valore segreto</span><span class="sxs-lookup"><span data-stu-id="2e7f3-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="2e7f3-112">Questo comando crea un **valore** denominato con un valore crittografato.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="2e7f3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e7f3-113">PARAMETERS</span></span>

### <span data-ttu-id="2e7f3-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2e7f3-114">-Context</span></span>
<span data-ttu-id="2e7f3-115">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2e7f3-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7f3-117">-DefaultProfile</span></span>
<span data-ttu-id="2e7f3-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e7f3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2e7f3-119">-Name</span></span>
<span data-ttu-id="2e7f3-120">Nome del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-120">Name of the named value.</span></span>
<span data-ttu-id="2e7f3-121">La lunghezza massima è 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="2e7f3-122">Può contenere solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="2e7f3-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7f3-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="2e7f3-124">-NamedValueId</span></span>
<span data-ttu-id="2e7f3-125">Identificatore del nuovo valore denominato.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-125">Identifier of new named value.</span></span>
<span data-ttu-id="2e7f3-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-126">This parameter is optional.</span></span>
<span data-ttu-id="2e7f3-127">Se non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="2e7f3-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="2e7f3-128">-Secret</span></span>
<span data-ttu-id="2e7f3-129">Determina se il valore è un segreto e deve essere crittografato o meno.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="2e7f3-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-130">This parameter is optional.</span></span>
<span data-ttu-id="2e7f3-131">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-131">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7f3-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e7f3-132">-Tag</span></span>
<span data-ttu-id="2e7f3-133">Tag da associare al valore denominato.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="2e7f3-134">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7f3-135">-Value</span><span class="sxs-lookup"><span data-stu-id="2e7f3-135">-Value</span></span>
<span data-ttu-id="2e7f3-136">Valore del valore denominato.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-136">Value of the named value.</span></span>
<span data-ttu-id="2e7f3-137">Può contenere espressioni per i criteri.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-137">Can contain policy expressions.</span></span>
<span data-ttu-id="2e7f3-138">La lunghezza massima è 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="2e7f3-139">Non può essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="2e7f3-140">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e7f3-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e7f3-141">-Confirm</span></span>
<span data-ttu-id="2e7f3-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e7f3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e7f3-143">-WhatIf</span></span>
<span data-ttu-id="2e7f3-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e7f3-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e7f3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7f3-146">CommonParameters</span></span>
<span data-ttu-id="2e7f3-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7f3-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e7f3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7f3-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e7f3-149">INPUTS</span></span>

### <span data-ttu-id="2e7f3-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e7f3-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e7f3-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2e7f3-151">System.String</span></span>

### <span data-ttu-id="2e7f3-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e7f3-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2e7f3-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2e7f3-153">System.String[]</span></span>

## <span data-ttu-id="2e7f3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e7f3-154">OUTPUTS</span></span>

### <span data-ttu-id="2e7f3-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2e7f3-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="2e7f3-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e7f3-156">NOTES</span></span>

## <span data-ttu-id="2e7f3-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e7f3-157">RELATED LINKS</span></span>
