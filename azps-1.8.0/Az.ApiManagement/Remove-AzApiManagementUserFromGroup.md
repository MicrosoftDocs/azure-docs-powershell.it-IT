---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 20c6894f91e92c6f70f5f753d26fe4d76a391e70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852425"
---
# <span data-ttu-id="c25ac-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="c25ac-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="c25ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c25ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c25ac-103">Rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="c25ac-103">Removes a user from a group.</span></span>

## <span data-ttu-id="c25ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c25ac-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c25ac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c25ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c25ac-106">Il cmdlet **Remove-AzApiManagementUserFromGroup** rimuove un utente da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="c25ac-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="c25ac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c25ac-107">EXAMPLES</span></span>

### <span data-ttu-id="c25ac-108">Esempio 1: rimuovere un utente da un gruppo</span><span class="sxs-lookup"><span data-stu-id="c25ac-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="c25ac-109">Questo comando rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="c25ac-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="c25ac-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c25ac-110">PARAMETERS</span></span>

### <span data-ttu-id="c25ac-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c25ac-111">-Context</span></span>
<span data-ttu-id="c25ac-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c25ac-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c25ac-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c25ac-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c25ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25ac-114">-DefaultProfile</span></span>
<span data-ttu-id="c25ac-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c25ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c25ac-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c25ac-116">-GroupId</span></span>
<span data-ttu-id="c25ac-117">Specifica l'ID del gruppo da cui rimuovere un utente.</span><span class="sxs-lookup"><span data-stu-id="c25ac-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="c25ac-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c25ac-118">-PassThru</span></span>
<span data-ttu-id="c25ac-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c25ac-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="c25ac-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="c25ac-120">-UserId</span></span>
<span data-ttu-id="c25ac-121">Specifica l'ID dell'utente da rimuovere dal gruppo.</span><span class="sxs-lookup"><span data-stu-id="c25ac-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="c25ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25ac-122">CommonParameters</span></span>
<span data-ttu-id="c25ac-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25ac-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25ac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25ac-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c25ac-125">INPUTS</span></span>

### <span data-ttu-id="c25ac-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c25ac-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c25ac-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c25ac-127">System.String</span></span>

### <span data-ttu-id="c25ac-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c25ac-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c25ac-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c25ac-129">OUTPUTS</span></span>

### <span data-ttu-id="c25ac-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c25ac-130">System.Boolean</span></span>

## <span data-ttu-id="c25ac-131">Note</span><span class="sxs-lookup"><span data-stu-id="c25ac-131">NOTES</span></span>

## <span data-ttu-id="c25ac-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c25ac-132">RELATED LINKS</span></span>

[<span data-ttu-id="c25ac-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="c25ac-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="c25ac-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c25ac-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


