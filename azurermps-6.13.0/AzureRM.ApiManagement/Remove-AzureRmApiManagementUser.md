---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 31ab005953ea405dc8aac093f973a6e842974814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519781"
---
# <span data-ttu-id="0686f-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0686f-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="0686f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0686f-102">SYNOPSIS</span></span>
<span data-ttu-id="0686f-103">Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="0686f-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0686f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0686f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0686f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0686f-105">DESCRIPTION</span></span>
<span data-ttu-id="0686f-106">Il cmdlet **Remove-AzureRmApiManagementUser** Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="0686f-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="0686f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0686f-107">EXAMPLES</span></span>

### <span data-ttu-id="0686f-108">Esempio 1: eliminare un utente</span><span class="sxs-lookup"><span data-stu-id="0686f-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="0686f-109">Questo comando Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="0686f-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="0686f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0686f-110">PARAMETERS</span></span>

### <span data-ttu-id="0686f-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0686f-111">-Context</span></span>
<span data-ttu-id="0686f-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0686f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0686f-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0686f-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0686f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0686f-114">-DefaultProfile</span></span>
<span data-ttu-id="0686f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0686f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0686f-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="0686f-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="0686f-117">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="0686f-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="0686f-118">Se questo parametro non viene specificato e esiste un abbonamento, questo cmdlet genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="0686f-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="0686f-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0686f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="0686f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0686f-120">-PassThru</span></span>
<span data-ttu-id="0686f-121">Indica che questo cmdlet restituisce un valore di $Ture, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0686f-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0686f-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="0686f-122">-UserId</span></span>
<span data-ttu-id="0686f-123">Specifica l'ID dell'utente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0686f-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="0686f-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0686f-124">-Confirm</span></span>
<span data-ttu-id="0686f-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0686f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0686f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0686f-126">-WhatIf</span></span>
<span data-ttu-id="0686f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0686f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0686f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0686f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0686f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0686f-129">CommonParameters</span></span>
<span data-ttu-id="0686f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0686f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0686f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0686f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0686f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0686f-132">INPUTS</span></span>

### <span data-ttu-id="0686f-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0686f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0686f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0686f-134">System.String</span></span>

### <span data-ttu-id="0686f-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0686f-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0686f-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0686f-136">OUTPUTS</span></span>

### <span data-ttu-id="0686f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0686f-137">System.Boolean</span></span>

## <span data-ttu-id="0686f-138">Note</span><span class="sxs-lookup"><span data-stu-id="0686f-138">NOTES</span></span>

## <span data-ttu-id="0686f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0686f-139">RELATED LINKS</span></span>

[<span data-ttu-id="0686f-140">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0686f-140">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="0686f-141">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0686f-141">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="0686f-142">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0686f-142">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


