---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: f8b96d8441e9a0b3a5f9b9bc3c775da7d71f12c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992416"
---
# <span data-ttu-id="93b50-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="93b50-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="93b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93b50-102">SYNOPSIS</span></span>
<span data-ttu-id="93b50-103">Elimina un contatto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93b50-103">Deletes a security contact.</span></span>

## <span data-ttu-id="93b50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93b50-104">SYNTAX</span></span>

### <span data-ttu-id="93b50-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="93b50-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93b50-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="93b50-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93b50-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="93b50-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93b50-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93b50-108">DESCRIPTION</span></span>
<span data-ttu-id="93b50-109">Elimina un contatto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="93b50-109">Deletes a security contact.</span></span>

## <span data-ttu-id="93b50-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93b50-110">EXAMPLES</span></span>

### <span data-ttu-id="93b50-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93b50-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="93b50-112">Elimina il contatto di sicurezza "default1"</span><span class="sxs-lookup"><span data-stu-id="93b50-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="93b50-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93b50-113">PARAMETERS</span></span>

### <span data-ttu-id="93b50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b50-114">-DefaultProfile</span></span>
<span data-ttu-id="93b50-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93b50-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93b50-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93b50-116">-InputObject</span></span>
<span data-ttu-id="93b50-117">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="93b50-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93b50-118">-Name</span><span class="sxs-lookup"><span data-stu-id="93b50-118">-Name</span></span>
<span data-ttu-id="93b50-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="93b50-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93b50-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93b50-120">-PassThru</span></span>
<span data-ttu-id="93b50-121">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="93b50-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="93b50-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93b50-122">-ResourceId</span></span>
<span data-ttu-id="93b50-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="93b50-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93b50-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93b50-124">-Confirm</span></span>
<span data-ttu-id="93b50-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93b50-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93b50-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93b50-126">-WhatIf</span></span>
<span data-ttu-id="93b50-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93b50-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93b50-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93b50-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93b50-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b50-129">CommonParameters</span></span>
<span data-ttu-id="93b50-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b50-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b50-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93b50-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b50-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="93b50-132">INPUTS</span></span>

### <span data-ttu-id="93b50-133">System.String</span><span class="sxs-lookup"><span data-stu-id="93b50-133">System.String</span></span>

### <span data-ttu-id="93b50-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="93b50-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="93b50-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93b50-135">OUTPUTS</span></span>

### <span data-ttu-id="93b50-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93b50-136">System.Boolean</span></span>

## <span data-ttu-id="93b50-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="93b50-137">NOTES</span></span>

## <span data-ttu-id="93b50-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93b50-138">RELATED LINKS</span></span>
