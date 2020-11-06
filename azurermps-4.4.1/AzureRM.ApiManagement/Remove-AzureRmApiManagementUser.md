---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508787"
---
# <span data-ttu-id="cb9a0-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cb9a0-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="cb9a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9a0-103">Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb9a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb9a0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb9a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9a0-106">Il cmdlet **Remove-AzureRmApiManagementUser** Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="cb9a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb9a0-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9a0-108">Esempio 1: eliminare un utente</span><span class="sxs-lookup"><span data-stu-id="cb9a0-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="cb9a0-109">Questo comando Elimina un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="cb9a0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb9a0-110">PARAMETERS</span></span>

### <span data-ttu-id="cb9a0-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cb9a0-111">-Context</span></span>
<span data-ttu-id="cb9a0-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cb9a0-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="cb9a0-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cb9a0-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="cb9a0-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="cb9a0-115">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="cb9a0-116">Se questo parametro non viene specificato e esiste un abbonamento, questo cmdlet genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="cb9a0-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb9a0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb9a0-118">-PassThru</span></span>
<span data-ttu-id="cb9a0-119">Indica che questo cmdlet restituisce un valore di $Ture, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="cb9a0-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="cb9a0-120">-UserId</span></span>
<span data-ttu-id="cb9a0-121">Specifica l'ID dell'utente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="cb9a0-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cb9a0-122">-Confirm</span></span>
<span data-ttu-id="cb9a0-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9a0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9a0-124">-WhatIf</span></span>
<span data-ttu-id="cb9a0-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9a0-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9a0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9a0-127">-DefaultProfile</span></span>
<span data-ttu-id="cb9a0-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9a0-129">CommonParameters</span></span>
<span data-ttu-id="cb9a0-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9a0-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9a0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9a0-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb9a0-132">INPUTS</span></span>

## <span data-ttu-id="cb9a0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb9a0-133">OUTPUTS</span></span>

### <span data-ttu-id="cb9a0-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="cb9a0-134">Boolean</span></span>

## <span data-ttu-id="cb9a0-135">Note</span><span class="sxs-lookup"><span data-stu-id="cb9a0-135">NOTES</span></span>

## <span data-ttu-id="cb9a0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb9a0-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb9a0-137">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cb9a0-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="cb9a0-138">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cb9a0-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="cb9a0-139">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cb9a0-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


