---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 17f7fe4046d5de9dfe288a96a00e8c03486e9c61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959038"
---
# <span data-ttu-id="7bc66-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7bc66-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="7bc66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bc66-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc66-103">Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="7bc66-103">Deletes an existing user.</span></span>

## <span data-ttu-id="7bc66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bc66-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bc66-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7bc66-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc66-106">Il cmdlet **Remove-AzApiManagementUser** elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="7bc66-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="7bc66-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bc66-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc66-108">Esempio 1: Eliminare un utente</span><span class="sxs-lookup"><span data-stu-id="7bc66-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="7bc66-109">Questo comando elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="7bc66-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="7bc66-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bc66-110">PARAMETERS</span></span>

### <span data-ttu-id="7bc66-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7bc66-111">-Context</span></span>
<span data-ttu-id="7bc66-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="7bc66-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7bc66-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="7bc66-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7bc66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc66-114">-DefaultProfile</span></span>
<span data-ttu-id="7bc66-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc66-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bc66-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="7bc66-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="7bc66-117">Indica se eliminare le sottoscrizioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="7bc66-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="7bc66-118">Se questo parametro non è specificato ed è presente una sottoscrizione, questo cmdlet genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="7bc66-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="7bc66-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7bc66-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="7bc66-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bc66-120">-PassThru</span></span>
<span data-ttu-id="7bc66-121">Indica che questo cmdlet restituisce il valore $Ture, se ha esito positivo, o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7bc66-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="7bc66-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="7bc66-122">-UserId</span></span>
<span data-ttu-id="7bc66-123">Specifica l'ID dell'utente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7bc66-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="7bc66-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bc66-124">-Confirm</span></span>
<span data-ttu-id="7bc66-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bc66-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc66-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc66-126">-WhatIf</span></span>
<span data-ttu-id="7bc66-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc66-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc66-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bc66-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc66-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc66-129">CommonParameters</span></span>
<span data-ttu-id="7bc66-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc66-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc66-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7bc66-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc66-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="7bc66-132">INPUTS</span></span>

### <span data-ttu-id="7bc66-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7bc66-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7bc66-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7bc66-134">System.String</span></span>

### <span data-ttu-id="7bc66-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7bc66-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7bc66-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bc66-136">OUTPUTS</span></span>

### <span data-ttu-id="7bc66-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7bc66-137">System.Boolean</span></span>

## <span data-ttu-id="7bc66-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="7bc66-138">NOTES</span></span>

## <span data-ttu-id="7bc66-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bc66-139">RELATED LINKS</span></span>

[<span data-ttu-id="7bc66-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7bc66-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="7bc66-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7bc66-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="7bc66-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7bc66-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


