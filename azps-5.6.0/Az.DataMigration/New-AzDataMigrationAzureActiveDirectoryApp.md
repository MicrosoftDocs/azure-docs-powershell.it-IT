---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 6fa598b792d04d8223aafdb39405a69ada6e5915
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966638"
---
# <span data-ttu-id="ec07f-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="ec07f-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="ec07f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec07f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec07f-103">Creare una nuova istanza dataMigration Azure ActiveDirectory Application details.</span><span class="sxs-lookup"><span data-stu-id="ec07f-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="ec07f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec07f-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec07f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ec07f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec07f-106">Creare una nuova istanza dataMigration Azure ActiveDirectory Application details.</span><span class="sxs-lookup"><span data-stu-id="ec07f-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="ec07f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec07f-107">EXAMPLES</span></span>

### <span data-ttu-id="ec07f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec07f-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="ec07f-109">ApplicationId: "Id AppId/ID entità servizio qui" AppKey : System.Security.SecureString TenantId : "ID tenant"</span><span class="sxs-lookup"><span data-stu-id="ec07f-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="ec07f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec07f-110">PARAMETERS</span></span>

### <span data-ttu-id="ec07f-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="ec07f-111">-AppKey</span></span>
<span data-ttu-id="ec07f-112">Chiave di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ec07f-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec07f-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ec07f-113">-ApplicationId</span></span>
<span data-ttu-id="ec07f-114">ID applicazione Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ec07f-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec07f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec07f-115">-DefaultProfile</span></span>
<span data-ttu-id="ec07f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec07f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec07f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec07f-117">CommonParameters</span></span>
<span data-ttu-id="ec07f-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec07f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ec07f-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec07f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec07f-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="ec07f-120">INPUTS</span></span>

### <span data-ttu-id="ec07f-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ec07f-121">None</span></span>

## <span data-ttu-id="ec07f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec07f-122">OUTPUTS</span></span>

### <span data-ttu-id="ec07f-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="ec07f-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="ec07f-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="ec07f-124">NOTES</span></span>

## <span data-ttu-id="ec07f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec07f-125">RELATED LINKS</span></span>
