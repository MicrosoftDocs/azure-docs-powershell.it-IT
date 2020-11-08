---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020085"
---
# <span data-ttu-id="71675-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="71675-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="71675-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71675-102">SYNOPSIS</span></span>
<span data-ttu-id="71675-103">Rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="71675-103">Removes a user from a group.</span></span>

## <span data-ttu-id="71675-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71675-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71675-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71675-105">DESCRIPTION</span></span>
<span data-ttu-id="71675-106">Il cmdlet **Remove-AzApiManagementUserFromGroup** rimuove un utente da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="71675-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="71675-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71675-107">EXAMPLES</span></span>

### <span data-ttu-id="71675-108">Esempio 1: rimuovere un utente da un gruppo</span><span class="sxs-lookup"><span data-stu-id="71675-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="71675-109">Questo comando rimuove un utente da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="71675-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="71675-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71675-110">PARAMETERS</span></span>

### <span data-ttu-id="71675-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="71675-111">-Context</span></span>
<span data-ttu-id="71675-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="71675-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="71675-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="71675-113">This parameter is required.</span></span>

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

### <span data-ttu-id="71675-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71675-114">-DefaultProfile</span></span>
<span data-ttu-id="71675-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71675-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71675-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="71675-116">-GroupId</span></span>
<span data-ttu-id="71675-117">Specifica l'ID del gruppo da cui rimuovere un utente.</span><span class="sxs-lookup"><span data-stu-id="71675-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="71675-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71675-118">-PassThru</span></span>
<span data-ttu-id="71675-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="71675-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="71675-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="71675-120">-UserId</span></span>
<span data-ttu-id="71675-121">Specifica l'ID dell'utente da rimuovere dal gruppo.</span><span class="sxs-lookup"><span data-stu-id="71675-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="71675-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71675-122">CommonParameters</span></span>
<span data-ttu-id="71675-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71675-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71675-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71675-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71675-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71675-125">INPUTS</span></span>

### <span data-ttu-id="71675-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="71675-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="71675-127">System. String</span><span class="sxs-lookup"><span data-stu-id="71675-127">System.String</span></span>

### <span data-ttu-id="71675-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71675-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71675-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71675-129">OUTPUTS</span></span>

### <span data-ttu-id="71675-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71675-130">System.Boolean</span></span>

## <span data-ttu-id="71675-131">Note</span><span class="sxs-lookup"><span data-stu-id="71675-131">NOTES</span></span>

## <span data-ttu-id="71675-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71675-132">RELATED LINKS</span></span>

[<span data-ttu-id="71675-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="71675-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="71675-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="71675-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


