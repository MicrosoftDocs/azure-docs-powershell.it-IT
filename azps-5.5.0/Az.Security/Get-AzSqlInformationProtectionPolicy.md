---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198726"
---
# <span data-ttu-id="5a9a0-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a9a0-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="5a9a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5a9a0-103">Recupera il tenant effettivo con i SQL di protezione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="5a9a0-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="5a9a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a9a0-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a9a0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="5a9a0-106">Recupera il tenant effettivo con i SQL di protezione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="5a9a0-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="5a9a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a9a0-107">EXAMPLES</span></span>

### <span data-ttu-id="5a9a0-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="5a9a0-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="5a9a0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a9a0-109">PARAMETERS</span></span>

### <span data-ttu-id="5a9a0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a9a0-110">-AsJob</span></span>
<span data-ttu-id="5a9a0-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5a9a0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a9a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a9a0-112">-DefaultProfile</span></span>
<span data-ttu-id="5a9a0-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a9a0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a9a0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a9a0-114">CommonParameters</span></span>
<span data-ttu-id="5a9a0-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a9a0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a9a0-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5a9a0-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a9a0-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a9a0-117">INPUTS</span></span>

### <span data-ttu-id="5a9a0-118">System.string</span><span class="sxs-lookup"><span data-stu-id="5a9a0-118">System.string</span></span>

## <span data-ttu-id="5a9a0-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a9a0-119">OUTPUTS</span></span>

### <span data-ttu-id="5a9a0-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a9a0-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="5a9a0-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a9a0-121">NOTES</span></span>

## <span data-ttu-id="5a9a0-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a9a0-122">RELATED LINKS</span></span>
