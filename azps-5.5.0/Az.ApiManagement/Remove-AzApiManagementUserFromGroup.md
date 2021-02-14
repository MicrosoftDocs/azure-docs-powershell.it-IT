---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197159"
---
# <span data-ttu-id="a8711-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="a8711-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="a8711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8711-102">SYNOPSIS</span></span>
<span data-ttu-id="a8711-103">Rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="a8711-103">Removes a user from a group.</span></span>

## <span data-ttu-id="a8711-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8711-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8711-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8711-105">DESCRIPTION</span></span>
<span data-ttu-id="a8711-106">Il cmdlet **Remove-AzApiManagementUserFromGroup** rimuove un utente da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="a8711-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="a8711-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8711-107">EXAMPLES</span></span>

### <span data-ttu-id="a8711-108">Esempio 1: Rimuovere un utente da un gruppo</span><span class="sxs-lookup"><span data-stu-id="a8711-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="a8711-109">Questo comando rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="a8711-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="a8711-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8711-110">PARAMETERS</span></span>

### <span data-ttu-id="a8711-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a8711-111">-Context</span></span>
<span data-ttu-id="a8711-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a8711-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a8711-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a8711-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a8711-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8711-114">-DefaultProfile</span></span>
<span data-ttu-id="a8711-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8711-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8711-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a8711-116">-GroupId</span></span>
<span data-ttu-id="a8711-117">Specifica l'ID del gruppo da cui rimuovere un utente.</span><span class="sxs-lookup"><span data-stu-id="a8711-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="a8711-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8711-118">-PassThru</span></span>
<span data-ttu-id="a8711-119">Indica che questo cmdlet restituisce il valore $True, se ha esito positivo, o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a8711-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="a8711-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="a8711-120">-UserId</span></span>
<span data-ttu-id="a8711-121">Specifica l'ID dell'utente da rimuovere dal gruppo.</span><span class="sxs-lookup"><span data-stu-id="a8711-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="a8711-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8711-122">CommonParameters</span></span>
<span data-ttu-id="a8711-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8711-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8711-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8711-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8711-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8711-125">INPUTS</span></span>

### <span data-ttu-id="a8711-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a8711-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a8711-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a8711-127">System.String</span></span>

### <span data-ttu-id="a8711-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8711-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8711-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8711-129">OUTPUTS</span></span>

### <span data-ttu-id="a8711-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8711-130">System.Boolean</span></span>

## <span data-ttu-id="a8711-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8711-131">NOTES</span></span>

## <span data-ttu-id="a8711-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8711-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8711-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="a8711-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="a8711-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a8711-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


