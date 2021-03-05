---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: da881ceac74810b05385b26f54b7c498c60c2e77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987530"
---
# <span data-ttu-id="3e490-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3e490-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="3e490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e490-102">SYNOPSIS</span></span>
<span data-ttu-id="3e490-103">Recupera il tenant effettivo con i SQL di protezione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="3e490-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="3e490-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e490-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e490-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e490-105">DESCRIPTION</span></span>
<span data-ttu-id="3e490-106">Recupera il tenant effettivo con i SQL di protezione delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="3e490-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="3e490-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e490-107">EXAMPLES</span></span>

### <span data-ttu-id="3e490-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="3e490-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="3e490-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e490-109">PARAMETERS</span></span>

### <span data-ttu-id="3e490-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e490-110">-AsJob</span></span>
<span data-ttu-id="3e490-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3e490-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e490-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e490-112">-DefaultProfile</span></span>
<span data-ttu-id="3e490-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e490-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e490-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e490-114">CommonParameters</span></span>
<span data-ttu-id="3e490-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e490-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e490-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e490-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e490-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e490-117">INPUTS</span></span>

### <span data-ttu-id="3e490-118">System.string</span><span class="sxs-lookup"><span data-stu-id="3e490-118">System.string</span></span>

## <span data-ttu-id="3e490-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e490-119">OUTPUTS</span></span>

### <span data-ttu-id="3e490-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3e490-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="3e490-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e490-121">NOTES</span></span>

## <span data-ttu-id="3e490-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e490-122">RELATED LINKS</span></span>
