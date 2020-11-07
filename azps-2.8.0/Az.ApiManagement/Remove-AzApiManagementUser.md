---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: d9c682f12bd56c2f862396670ce77a8730712279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675922"
---
# <span data-ttu-id="aed36-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aed36-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="aed36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aed36-102">SYNOPSIS</span></span>
<span data-ttu-id="aed36-103">Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="aed36-103">Deletes an existing user.</span></span>

## <span data-ttu-id="aed36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aed36-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed36-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aed36-105">DESCRIPTION</span></span>
<span data-ttu-id="aed36-106">Il cmdlet **Remove-AzApiManagementUser** Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="aed36-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="aed36-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aed36-107">EXAMPLES</span></span>

### <span data-ttu-id="aed36-108">Esempio 1: eliminare un utente</span><span class="sxs-lookup"><span data-stu-id="aed36-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="aed36-109">Questo comando Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="aed36-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="aed36-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aed36-110">PARAMETERS</span></span>

### <span data-ttu-id="aed36-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="aed36-111">-Context</span></span>
<span data-ttu-id="aed36-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="aed36-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="aed36-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="aed36-113">This parameter is required.</span></span>

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

### <span data-ttu-id="aed36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed36-114">-DefaultProfile</span></span>
<span data-ttu-id="aed36-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aed36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed36-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="aed36-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="aed36-117">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="aed36-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="aed36-118">Se questo parametro non viene specificato e esiste un abbonamento, questo cmdlet genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="aed36-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="aed36-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="aed36-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="aed36-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aed36-120">-PassThru</span></span>
<span data-ttu-id="aed36-121">Indica che questo cmdlet restituisce un valore di $Ture, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aed36-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="aed36-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="aed36-122">-UserId</span></span>
<span data-ttu-id="aed36-123">Specifica l'ID dell'utente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="aed36-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="aed36-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aed36-124">-Confirm</span></span>
<span data-ttu-id="aed36-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aed36-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed36-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed36-126">-WhatIf</span></span>
<span data-ttu-id="aed36-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aed36-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aed36-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aed36-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed36-129">CommonParameters</span></span>
<span data-ttu-id="aed36-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed36-131">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aed36-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed36-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aed36-132">INPUTS</span></span>

### <span data-ttu-id="aed36-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aed36-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aed36-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aed36-134">System.String</span></span>

### <span data-ttu-id="aed36-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aed36-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aed36-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aed36-136">OUTPUTS</span></span>

### <span data-ttu-id="aed36-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aed36-137">System.Boolean</span></span>

## <span data-ttu-id="aed36-138">Note</span><span class="sxs-lookup"><span data-stu-id="aed36-138">NOTES</span></span>

## <span data-ttu-id="aed36-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aed36-139">RELATED LINKS</span></span>

[<span data-ttu-id="aed36-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aed36-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="aed36-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aed36-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="aed36-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="aed36-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)

