---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 49b86055c185dd474499cf8674a34668f69ee060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675881"
---
# <span data-ttu-id="b6c5b-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6c5b-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="b6c5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c5b-103">Modifica una proprietà di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="b6c5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6c5b-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6c5b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6c5b-105">DESCRIPTION</span></span>
<span data-ttu-id="b6c5b-106">Il cmdlet **set-AzApiManagementProperty** modifica una proprietà di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="b6c5b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6c5b-107">EXAMPLES</span></span>

### <span data-ttu-id="b6c5b-108">Esempio 1: modificare i tag in una proprietà</span><span class="sxs-lookup"><span data-stu-id="b6c5b-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="b6c5b-109">Il primo comando assegna due valori alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="b6c5b-110">Il secondo comando modifica la proprietà che contiene l'ID Property11.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="b6c5b-111">Il comando assegna le stringhe in $Tags come tag nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="b6c5b-112">Esempio 2: modificare una proprietà per avere un valore segreto</span><span class="sxs-lookup"><span data-stu-id="b6c5b-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="b6c5b-113">Questo comando modifica la proprietà da crittografare.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="b6c5b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6c5b-114">PARAMETERS</span></span>

### <span data-ttu-id="b6c5b-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b6c5b-115">-Context</span></span>
<span data-ttu-id="b6c5b-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b6c5b-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b6c5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c5b-117">-DefaultProfile</span></span>
<span data-ttu-id="b6c5b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6c5b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6c5b-119">-Name</span></span>
<span data-ttu-id="b6c5b-120">Specifica il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-120">Specifies the name of the property.</span></span>
<span data-ttu-id="b6c5b-121">La lunghezza massima è di 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="b6c5b-122">I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="b6c5b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6c5b-123">-PassThru</span></span>
<span data-ttu-id="b6c5b-124">Indica che questo cmdlet restituisce il **PsApiManagementProperty** modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6c5b-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="b6c5b-125">-PropertyId</span></span>
<span data-ttu-id="b6c5b-126">Specifica un ID della proprietà modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6c5b-127">-Segreto</span><span class="sxs-lookup"><span data-stu-id="b6c5b-127">-Secret</span></span>
<span data-ttu-id="b6c5b-128">Indica che il valore della proprietà è un segreto e deve essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c5b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6c5b-129">-Tag</span></span>
<span data-ttu-id="b6c5b-130">Tag associati a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-130">Tags associated with a property.</span></span> <span data-ttu-id="b6c5b-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="b6c5b-132">-Valore</span><span class="sxs-lookup"><span data-stu-id="b6c5b-132">-Value</span></span>
<span data-ttu-id="b6c5b-133">Specifica un valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-133">Specifies a value for the property.</span></span>
<span data-ttu-id="b6c5b-134">Questo valore può contenere espressioni di criteri.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="b6c5b-135">La lunghezza massima è di 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="b6c5b-136">Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="b6c5b-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6c5b-137">-Confirm</span></span>
<span data-ttu-id="b6c5b-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c5b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c5b-139">-WhatIf</span></span>
<span data-ttu-id="b6c5b-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6c5b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c5b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c5b-142">CommonParameters</span></span>
<span data-ttu-id="b6c5b-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c5b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c5b-144">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6c5b-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c5b-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6c5b-145">INPUTS</span></span>

### <span data-ttu-id="b6c5b-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b6c5b-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b6c5b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b6c5b-147">System.String</span></span>

### <span data-ttu-id="b6c5b-148">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b6c5b-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b6c5b-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="b6c5b-149">System.String[]</span></span>

### <span data-ttu-id="b6c5b-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6c5b-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6c5b-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6c5b-151">OUTPUTS</span></span>

### <span data-ttu-id="b6c5b-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6c5b-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="b6c5b-153">Note</span><span class="sxs-lookup"><span data-stu-id="b6c5b-153">NOTES</span></span>

## <span data-ttu-id="b6c5b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6c5b-154">RELATED LINKS</span></span>

[<span data-ttu-id="b6c5b-155">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6c5b-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="b6c5b-156">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6c5b-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="b6c5b-157">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b6c5b-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


